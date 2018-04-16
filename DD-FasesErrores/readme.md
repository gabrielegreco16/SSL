
2)	
	COMANDO EN LA CONSOLA:
	cc hello2.c -E -P -o hello2.i

	
typedef long unsigned int size_t;
typedef unsigned char __u_char;
typedef unsigned short int __u_short;
typedef unsigned int __u_int;
typedef unsigned long int __u_long;
typedef signed char __int8_t;
typedef unsigned char __uint8_t;
typedef signed short int __int16_t;
typedef unsigned short int __uint16_t;
typedef signed int __int32_t;
typedef unsigned int __uint32_t;
typedef signed long int __int64_t;
typedef unsigned long int __uint64_t;
typedef long int __quad_t;
typedef unsigned long int __u_quad_t;
typedef unsigned long int __dev_t;
typedef unsigned int __uid_t;
typedef unsigned int __gid_t;
typedef unsigned long int __ino_t;
typedef unsigned long int __ino64_t;
typedef unsigned int __mode_t;
typedef unsigned long int __nlink_t;
typedef long int __off_t;
typedef long int __off64_t;
typedef int __pid_t;
typedef struct { int __val[2]; } __fsid_t;
typedef long int __clock_t;
typedef unsigned long int __rlim_t;
typedef unsigned long int __rlim64_t;
typedef unsigned int __id_t;
typedef long int __time_t;
typedef unsigned int __useconds_t;
typedef long int __suseconds_t;
typedef int __daddr_t;
typedef int __key_t;
typedef int __clockid_t;
typedef void * __timer_t;
typedef long int __blksize_t;
typedef long int __blkcnt_t;
typedef long int __blkcnt64_t;
typedef unsigned long int __fsblkcnt_t;
typedef unsigned long int __fsblkcnt64_t;
typedef unsigned long int __fsfilcnt_t;
typedef unsigned long int __fsfilcnt64_t;
typedef long int __fsword_t;
typedef long int __ssize_t;
typedef long int __syscall_slong_t;
typedef unsigned long int __syscall_ulong_t;
typedef __off64_t __loff_t;
typedef __quad_t *__qaddr_t;
typedef char *__caddr_t;
typedef long int __intptr_t;
typedef unsigned int __socklen_t;
struct _IO_FILE;

typedef struct _IO_FILE FILE;


typedef struct _IO_FILE __FILE;
typedef struct
{
  int __count;
  union
  {
    unsigned int __wch;
    char __wchb[4];
  } __value;
} __mbstate_t;
typedef struct
{
  __off_t __pos;
  __mbstate_t __state;
} _G_fpos_t;
typedef struct
{
  __off64_t __pos;
  __mbstate_t __state;
} _G_fpos64_t;
typedef __builtin_va_list __gnuc_va_list;
struct _IO_jump_t; struct _IO_FILE;
typedef void _IO_lock_t;
struct _IO_marker {
  struct _IO_marker *_next;
  struct _IO_FILE *_sbuf;
  int _pos;
};
enum __codecvt_result
{
  __codecvt_ok,
  __codecvt_partial,
  __codecvt_error,
  __codecvt_noconv
};
struct _IO_FILE {
  int _flags;
  char* _IO_read_ptr;
  char* _IO_read_end;
  char* _IO_read_base;
  char* _IO_write_base;
  char* _IO_write_ptr;
  char* _IO_write_end;
  char* _IO_buf_base;
  char* _IO_buf_end;
  char *_IO_save_base;
  char *_IO_backup_base;
  char *_IO_save_end;
  struct _IO_marker *_markers;
  struct _IO_FILE *_chain;
  int _fileno;
  int _flags2;
  __off_t _old_offset;
  unsigned short _cur_column;
  signed char _vtable_offset;
  char _shortbuf[1];
  _IO_lock_t *_lock;
  __off64_t _offset;
  void *__pad1;
  void *__pad2;
  void *__pad3;
  void *__pad4;
  size_t __pad5;
  int _mode;
  char _unused2[15 * sizeof (int) - 4 * sizeof (void *) - sizeof (size_t)];
};
typedef struct _IO_FILE _IO_FILE;
struct _IO_FILE_plus;
extern struct _IO_FILE_plus _IO_2_1_stdin_;
extern struct _IO_FILE_plus _IO_2_1_stdout_;
extern struct _IO_FILE_plus _IO_2_1_stderr_;
typedef __ssize_t __io_read_fn (void *__cookie, char *__buf, size_t __nbytes);
typedef __ssize_t __io_write_fn (void *__cookie, const char *__buf,
     size_t __n);
typedef int __io_seek_fn (void *__cookie, __off64_t *__pos, int __w);
typedef int __io_close_fn (void *__cookie);
extern int __underflow (_IO_FILE *);
extern int __uflow (_IO_FILE *);
extern int __overflow (_IO_FILE *, int);
extern int _IO_getc (_IO_FILE *__fp);
extern int _IO_putc (int __c, _IO_FILE *__fp);
extern int _IO_feof (_IO_FILE *__fp) __attribute__ ((__nothrow__ , __leaf__));
extern int _IO_ferror (_IO_FILE *__fp) __attribute__ ((__nothrow__ , __leaf__));
extern int _IO_peekc_locked (_IO_FILE *__fp);
extern void _IO_flockfile (_IO_FILE *) __attribute__ ((__nothrow__ , __leaf__));
extern void _IO_funlockfile (_IO_FILE *) __attribute__ ((__nothrow__ , __leaf__));
extern int _IO_ftrylockfile (_IO_FILE *) __attribute__ ((__nothrow__ , __leaf__));
extern int _IO_vfscanf (_IO_FILE * __restrict, const char * __restrict,
   __gnuc_va_list, int *__restrict);
extern int _IO_vfprintf (_IO_FILE *__restrict, const char *__restrict,
    __gnuc_va_list);
extern __ssize_t _IO_padn (_IO_FILE *, int, __ssize_t);
extern size_t _IO_sgetn (_IO_FILE *, void *, size_t);
extern __off64_t _IO_seekoff (_IO_FILE *, __off64_t, int, int);
extern __off64_t _IO_seekpos (_IO_FILE *, __off64_t, int);
extern void _IO_free_backup_area (_IO_FILE *) __attribute__ ((__nothrow__ , __leaf__));
typedef __gnuc_va_list va_list;
typedef __off_t off_t;
typedef __ssize_t ssize_t;

typedef _G_fpos_t fpos_t;

extern struct _IO_FILE *stdin;
extern struct _IO_FILE *stdout;
extern struct _IO_FILE *stderr;

extern int remove (const char *__filename) __attribute__ ((__nothrow__ , __leaf__));
extern int rename (const char *__old, const char *__new) __attribute__ ((__nothrow__ , __leaf__));

extern int renameat (int __oldfd, const char *__old, int __newfd,
       const char *__new) __attribute__ ((__nothrow__ , __leaf__));

extern FILE *tmpfile (void) ;
extern char *tmpnam (char *__s) __attribute__ ((__nothrow__ , __leaf__)) ;

extern char *tmpnam_r (char *__s) __attribute__ ((__nothrow__ , __leaf__)) ;
extern char *tempnam (const char *__dir, const char *__pfx)
     __attribute__ ((__nothrow__ , __leaf__)) __attribute__ ((__malloc__)) ;

extern int fclose (FILE *__stream);
extern int fflush (FILE *__stream);

extern int fflush_unlocked (FILE *__stream);

extern FILE *fopen (const char *__restrict __filename,
      const char *__restrict __modes) ;
extern FILE *freopen (const char *__restrict __filename,
        const char *__restrict __modes,
        FILE *__restrict __stream) ;

extern FILE *fdopen (int __fd, const char *__modes) __attribute__ ((__nothrow__ , __leaf__)) ;
extern FILE *fmemopen (void *__s, size_t __len, const char *__modes)
  __attribute__ ((__nothrow__ , __leaf__)) ;
extern FILE *open_memstream (char **__bufloc, size_t *__sizeloc) __attribute__ ((__nothrow__ , __leaf__)) ;

extern void setbuf (FILE *__restrict __stream, char *__restrict __buf) __attribute__ ((__nothrow__ , __leaf__));
extern int setvbuf (FILE *__restrict __stream, char *__restrict __buf,
      int __modes, size_t __n) __attribute__ ((__nothrow__ , __leaf__));

extern void setbuffer (FILE *__restrict __stream, char *__restrict __buf,
         size_t __size) __attribute__ ((__nothrow__ , __leaf__));
extern void setlinebuf (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__));

extern int fprintf (FILE *__restrict __stream,
      const char *__restrict __format, ...);
extern int printf (const char *__restrict __format, ...);
extern int sprintf (char *__restrict __s,
      const char *__restrict __format, ...) __attribute__ ((__nothrow__));
extern int vfprintf (FILE *__restrict __s, const char *__restrict __format,
       __gnuc_va_list __arg);
extern int vprintf (const char *__restrict __format, __gnuc_va_list __arg);
extern int vsprintf (char *__restrict __s, const char *__restrict __format,
       __gnuc_va_list __arg) __attribute__ ((__nothrow__));


extern int snprintf (char *__restrict __s, size_t __maxlen,
       const char *__restrict __format, ...)
     __attribute__ ((__nothrow__)) __attribute__ ((__format__ (__printf__, 3, 4)));
extern int vsnprintf (char *__restrict __s, size_t __maxlen,
        const char *__restrict __format, __gnuc_va_list __arg)
     __attribute__ ((__nothrow__)) __attribute__ ((__format__ (__printf__, 3, 0)));

extern int vdprintf (int __fd, const char *__restrict __fmt,
       __gnuc_va_list __arg)
     __attribute__ ((__format__ (__printf__, 2, 0)));
extern int dprintf (int __fd, const char *__restrict __fmt, ...)
     __attribute__ ((__format__ (__printf__, 2, 3)));

extern int fscanf (FILE *__restrict __stream,
     const char *__restrict __format, ...) ;
extern int scanf (const char *__restrict __format, ...) ;
extern int sscanf (const char *__restrict __s,
     const char *__restrict __format, ...) __attribute__ ((__nothrow__ , __leaf__));
extern int fscanf (FILE *__restrict __stream, const char *__restrict __format, ...) __asm__ ("" "__isoc99_fscanf") ;
extern int scanf (const char *__restrict __format, ...) __asm__ ("" "__isoc99_scanf") ;
extern int sscanf (const char *__restrict __s, const char *__restrict __format, ...) __asm__ ("" "__isoc99_sscanf") __attribute__ ((__nothrow__ , __leaf__));


extern int vfscanf (FILE *__restrict __s, const char *__restrict __format,
      __gnuc_va_list __arg)
     __attribute__ ((__format__ (__scanf__, 2, 0))) ;
extern int vscanf (const char *__restrict __format, __gnuc_va_list __arg)
     __attribute__ ((__format__ (__scanf__, 1, 0))) ;
extern int vsscanf (const char *__restrict __s,
      const char *__restrict __format, __gnuc_va_list __arg)
     __attribute__ ((__nothrow__ , __leaf__)) __attribute__ ((__format__ (__scanf__, 2, 0)));
extern int vfscanf (FILE *__restrict __s, const char *__restrict __format, __gnuc_va_list __arg) __asm__ ("" "__isoc99_vfscanf")
     __attribute__ ((__format__ (__scanf__, 2, 0))) ;
extern int vscanf (const char *__restrict __format, __gnuc_va_list __arg) __asm__ ("" "__isoc99_vscanf")
     __attribute__ ((__format__ (__scanf__, 1, 0))) ;
extern int vsscanf (const char *__restrict __s, const char *__restrict __format, __gnuc_va_list __arg) __asm__ ("" "__isoc99_vsscanf") __attribute__ ((__nothrow__ , __leaf__))
     __attribute__ ((__format__ (__scanf__, 2, 0)));


extern int fgetc (FILE *__stream);
extern int getc (FILE *__stream);
extern int getchar (void);

extern int getc_unlocked (FILE *__stream);
extern int getchar_unlocked (void);
extern int fgetc_unlocked (FILE *__stream);

extern int fputc (int __c, FILE *__stream);
extern int putc (int __c, FILE *__stream);
extern int putchar (int __c);

extern int fputc_unlocked (int __c, FILE *__stream);
extern int putc_unlocked (int __c, FILE *__stream);
extern int putchar_unlocked (int __c);
extern int getw (FILE *__stream);
extern int putw (int __w, FILE *__stream);

extern char *fgets (char *__restrict __s, int __n, FILE *__restrict __stream)
     ;

extern __ssize_t __getdelim (char **__restrict __lineptr,
          size_t *__restrict __n, int __delimiter,
          FILE *__restrict __stream) ;
extern __ssize_t getdelim (char **__restrict __lineptr,
        size_t *__restrict __n, int __delimiter,
        FILE *__restrict __stream) ;
extern __ssize_t getline (char **__restrict __lineptr,
       size_t *__restrict __n,
       FILE *__restrict __stream) ;

extern int fputs (const char *__restrict __s, FILE *__restrict __stream);
extern int puts (const char *__s);
extern int ungetc (int __c, FILE *__stream);
extern size_t fread (void *__restrict __ptr, size_t __size,
       size_t __n, FILE *__restrict __stream) ;
extern size_t fwrite (const void *__restrict __ptr, size_t __size,
        size_t __n, FILE *__restrict __s);

extern size_t fread_unlocked (void *__restrict __ptr, size_t __size,
         size_t __n, FILE *__restrict __stream) ;
extern size_t fwrite_unlocked (const void *__restrict __ptr, size_t __size,
          size_t __n, FILE *__restrict __stream);

extern int fseek (FILE *__stream, long int __off, int __whence);
extern long int ftell (FILE *__stream) ;
extern void rewind (FILE *__stream);

extern int fseeko (FILE *__stream, __off_t __off, int __whence);
extern __off_t ftello (FILE *__stream) ;

extern int fgetpos (FILE *__restrict __stream, fpos_t *__restrict __pos);
extern int fsetpos (FILE *__stream, const fpos_t *__pos);


extern void clearerr (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__));
extern int feof (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;
extern int ferror (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;

extern void clearerr_unlocked (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__));
extern int feof_unlocked (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;
extern int ferror_unlocked (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;

extern void perror (const char *__s);

extern int sys_nerr;
extern const char *const sys_errlist[];
extern int fileno (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;
extern int fileno_unlocked (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;
extern FILE *popen (const char *__command, const char *__modes) ;
extern int pclose (FILE *__stream);
extern char *ctermid (char *__s) __attribute__ ((__nothrow__ , __leaf__));
extern void flockfile (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__));
extern int ftrylockfile (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__)) ;
extern void funlockfile (FILE *__stream) __attribute__ ((__nothrow__ , __leaf__));

int main(void){
int i=42;
 prontf("La respuesta es %d\n");

 Ademas de tener las mismas sentecias de hello3.c tiene toda la bibleoteca de manera explicita

4) 	
	En la primera linea de hello3.c printf entrega un int y le pasamos un puntero constante a char y los puntos   
	suspensivos significan que tiene un número indeterminado de argumentos. Para eso hay que declarar los parámetros conocidos de modo normal, debe existir al menos un parámetro de este tipo. Los parámetros desconocidos se sustituyen por tres puntos (...)

5)
COMANDO EN LA CONSOLA:
	cc hello3.c -E  -o hello3.i

	# 1 "hello3.c"
# 1 "<built-in>"
# 1 "<command-line>"
# 1 "/usr/include/stdc-predef.h" 1 3 4
# 1 "<command-line>" 2
# 1 "hello3.c"
int printf(const char *s, ...);
int main(void){
int i=42;
 prontf("La respuesta es %d\n");

	ademas de tener las mismas sentecias de hello3.c tiene toda la bibleoteca de manera explicita.

6) 
COMANDO EN LA CONSOLA:
	cc hello3.i -S

hello3.c: In function ‘main’:
hello3.c:4:2: warning: implicit declaration of function ‘prontf’ [-Wimplicit-function-declaration]
  prontf("La respuesta es %d\n");
  ^
hello3.c:4:2: error: expected declaration or statement at end of input

espera una declaracion de la funcion prontf() pero no la encuentra.

7) COMANDOS EN LA CONSOLA:
	 cc hello4.c -E -P -o hello4.i
	 cc hello4.i -S

	 por consola no aparece nada la salida se guarda en el hello4.s

8) hello4.s =

		.file	"hello4.i"
	.section	.rodata
.LC0:
	.string	"La respuesta es "
	.text
	.globl	main
	.type	main, @function
main:
.LFB0:
	.cfi_startproc
	pushq	%rbp
	.cfi_def_cfa_offset 16
	.cfi_offset 6, -16
	movq	%rsp, %rbp
	.cfi_def_cfa_register 6
	subq	$16, %rsp
	movl	$42, -4(%rbp)
	movl	$.LC0, %edi
	movl	$0, %eax
	call	printf
	movl	$0, %eax
	leave
	.cfi_def_cfa 7, 8
	ret
	.cfi_endproc
.LFE0:
	.size	main, .-main
	.ident	"GCC: (Ubuntu 5.4.0-6ubuntu1~16.04.9) 5.4.0 20160609"
	.section	.note.GNU-stack,"",@progbits

	lo que se peude ver a simple vista el que el hello4.s tiene mas sentencias que el hello4.c sabiendo los mnemonicos del micro para el cual se genera el assembly puedo ir sabiendo que hace en cada sentencia.

9)	
 cc hello4.s -c

 genero el codigo objeto

 el contenido de hello4.o  es:

 7f45 4c46 0201 0100 0000 0000 0000 0000
0100 3e00 0100 0000 0000 0000 0000 0000
0000 0000 0000 0000 b802 0000 0000 0000
0000 0000 4000 0000 0000 4000 0d00 0a00
5548 89e5 4883 ec10 c745 fc2a 0000 00bf
0000 0000 b800 0000 00e8 0000 0000 b800
0000 00c9 c34c 6120 7265 7370 7565 7374
6120 6573 2000 0047 4343 3a20 2855 6275
6e74 7520 352e 342e 302d 3675 6275 6e74
7531 7e31 362e 3034 2e39 2920 352e 342e
3020 3230 3136 3036 3039 0000 0000 0000
1400 0000 0000 0000 017a 5200 0178 1001
1b0c 0708 9001 0000 1c00 0000 1c00 0000
0000 0000 2500 0000 0041 0e10 8602 430d
0660 0c07 0800 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0100 0000 0400 f1ff 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0300 0100
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0300 0300 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0300 0400
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0300 0500 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0300 0700
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0300 0800 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0300 0600
0000 0000 0000 0000 0000 0000 0000 0000
0a00 0000 1200 0100 0000 0000 0000 0000
2500 0000 0000 0000 0f00 0000 1000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0068 656c 6c6f 342e 6900 6d61 696e 0070
7269 6e74 6600 0000 1000 0000 0000 0000
0a00 0000 0500 0000 0000 0000 0000 0000
1a00 0000 0000 0000 0200 0000 0a00 0000
fcff ffff ffff ffff 2000 0000 0000 0000
0200 0000 0200 0000 0000 0000 0000 0000
002e 7379 6d74 6162 002e 7374 7274 6162
002e 7368 7374 7274 6162 002e 7265 6c61
2e74 6578 7400 2e64 6174 6100 2e62 7373
002e 726f 6461 7461 002e 636f 6d6d 656e
7400 2e6e 6f74 652e 474e 552d 7374 6163
6b00 2e72 656c 612e 6568 5f66 7261 6d65
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 2000 0000 0100 0000
0600 0000 0000 0000 0000 0000 0000 0000
4000 0000 0000 0000 2500 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 1b00 0000 0400 0000
4000 0000 0000 0000 0000 0000 0000 0000
0802 0000 0000 0000 3000 0000 0000 0000
0b00 0000 0100 0000 0800 0000 0000 0000
1800 0000 0000 0000 2600 0000 0100 0000
0300 0000 0000 0000 0000 0000 0000 0000
6500 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 2c00 0000 0800 0000
0300 0000 0000 0000 0000 0000 0000 0000
6500 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 3100 0000 0100 0000
0200 0000 0000 0000 0000 0000 0000 0000
6500 0000 0000 0000 1100 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 3900 0000 0100 0000
3000 0000 0000 0000 0000 0000 0000 0000
7600 0000 0000 0000 3500 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0100 0000 0000 0000 4200 0000 0100 0000
0000 0000 0000 0000 0000 0000 0000 0000
ab00 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 5700 0000 0100 0000
0200 0000 0000 0000 0000 0000 0000 0000
b000 0000 0000 0000 3800 0000 0000 0000
0000 0000 0000 0000 0800 0000 0000 0000
0000 0000 0000 0000 5200 0000 0400 0000
4000 0000 0000 0000 0000 0000 0000 0000
3802 0000 0000 0000 1800 0000 0000 0000
0b00 0000 0800 0000 0800 0000 0000 0000
1800 0000 0000 0000 1100 0000 0300 0000
0000 0000 0000 0000 0000 0000 0000 0000
5002 0000 0000 0000 6100 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 0100 0000 0200 0000
0000 0000 0000 0000 0000 0000 0000 0000
e800 0000 0000 0000 0801 0000 0000 0000
0c00 0000 0900 0000 0800 0000 0000 0000
1800 0000 0000 0000 0900 0000 0300 0000
0000 0000 0000 0000 0000 0000 0000 0000
f001 0000 0000 0000 1600 0000 0000 0000
0000 0000 0000 0000 0100 0000 0000 0000
0000 0000 0000 0000 

10)

	Genero el ejecutable:

	cc hello4.o -o hello4

11)No pude darme cuenta como hacer para que falle en querer general el ejecutable el hello4.o , lo mismo con el 12) y 13)


15) el hello7.c se le agrego el parametro de entrada i em el printf y se cerro la funcion en el main con llave.