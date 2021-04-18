---
title: Ändern von Elementen von Benutzerinformationen
description: Die Netzwerk Verwaltungsfunktionen stellen eine Vielzahl von Informationsebenen bereit, um das Ändern von Benutzerinformationen zu unterstützen.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339072"
---
# <a name="changing-elements-of-user-information"></a>Ändern von Elementen von Benutzerinformationen

Die Netzwerk Verwaltungsfunktionen stellen eine Vielzahl von Informationsebenen bereit, um das Ändern von Benutzerinformationen zu unterstützen. Einige Ebenen erfordern Administratorrechte, um erfolgreich ausgeführt zu werden. Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

Der Beispielcode in diesem Thema veranschaulicht, wie mehrere Elemente von Benutzerinformationen durch Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " geändert werden. Der Code verwendet verschiedene Netzwerk Verwaltungs Informationsstrukturen.

Wenn Sie Benutzerinformationen ändern, empfiehlt es sich, eine bestimmte Ebene für diese Informationen zu verwenden. Dadurch wird verhindert, dass nicht verknüpfte Informationen versehentlich zurückgesetzt werden, wenn die Werte der niedrigeren Ebene verwendet werden.

Das Festlegen einiger der häufig verwendeten Ebenen ist in den folgenden Codebeispielen dargestellt:

-   [Festlegen des Benutzer Kennworts, Ebene 1003](#setting-the-user-password-level-1003)
-   [Festlegen der Benutzer Berechtigung, Ebene 1005](#setting-the-user-privilege-level-1005)
-   [Festlegen des Basisverzeichnisses des Benutzers, Ebene 1006](#setting-the-user-home-directory-level-1006)
-   [Festlegen des Benutzer Kommentar Felds, Ebene 1007](#setting-the-user-comment-field-level-1007)
-   [Festlegen der Benutzerflags, Ebene 1008](#setting-the-user-flags-level-1008)
-   [Festlegen des Benutzer Skript Pfads, Ebene 1009](#setting-the-user-script-path-level-1009)
-   [Festlegen der benutzerautorierungsflags, Ebene 1010](#setting-the-user-authority-flags-level-1010)
-   [Festlegen des vollständigen Benutzernamens, Ebene 1011](#setting-the-user-full-name-level-1011)

Alle Code Fragmente gehen davon aus, dass der Benutzer die Unicode-Kompilierungs Direktive definiert und die entsprechenden SDK-Header Dateien wie folgt eingefügt hat:


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a>Festlegen des Benutzer Kennworts, Ebene 1003

Das folgende Code Fragment veranschaulicht, wie das Kennwort eines Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " auf einen bekannten Wert festgelegt wird. Das Thema [**Benutzer \_ Info \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) enthält weitere Informationen.


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a>Festlegen der Benutzer Berechtigung, Ebene 1005

Das folgende Code Fragment veranschaulicht, wie die Ebene der Berechtigung, die einem Benutzer zugewiesen wird, mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " angegeben wird. Das Thema [**Benutzer \_ Info \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) enthält weitere Informationen. Weitere Informationen zu Konto Berechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges) und [Autorisierungs Konstanten](/windows/desktop/SecAuthZ/authorization-constants).


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a>Festlegen des Basisverzeichnisses des Benutzers, Ebene 1006

Das folgende Code Fragment veranschaulicht, wie der Pfad des Basisverzeichnisses eines Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " angegeben wird. Bei dem Verzeichnis kann es sich um einen hart codierten Pfad oder um einen gültigen Unicode-Pfad handeln. Das Thema [**Benutzer \_ Info \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) enthält weitere Informationen.


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a>Festlegen des Benutzer Kommentar Felds, Ebene 1007

Das folgende Code Fragment veranschaulicht, wie ein Kommentar einem Benutzer zugeordnet wird, indem die Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " aufgerufen wird. Das Thema [**Benutzer \_ Info \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) enthält weitere Informationen.


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a>Festlegen der Benutzerflags, Ebene 1008

Das folgende Code Fragment veranschaulicht, wie Benutzerflags mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt werden. Das Thema [**Benutzer \_ Info \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) enthält eine Liste gültiger Werte für die Flags und eine Beschreibung der einzelnen Flags.

Beachten Sie, dass das \_ kennflag für das Angleichen Skript für Windows NT-, Windows 2000-, Windows XP-und LAN Manager-Netzwerke festgelegt werden muss Wenn Sie versuchen, andere Flags festzulegen, ohne ein "UF- \_ Skript" auf diese Netzwerke festzulegen, schlägt die Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " fehl


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a>Festlegen des Benutzer Skript Pfads, Ebene 1009

Das folgende Code Fragment veranschaulicht, wie der Pfad für die Anmelde Skriptdatei eines bestimmten Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt wird. Die Skriptdatei kann ein sein. Cmd-Datei, eine. EXE-Datei oder ein. BAT-Datei. Die Zeichenfolge kann auch NULL sein. Das Thema [**Benutzer \_ Info \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) enthält weitere Informationen.


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a>Festlegen der benutzerautorierungsflags, Ebene 1010

Das folgende Code Fragment veranschaulicht, wie die Operatoren für Operator Privilegien für einen Benutzer mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt werden. Das Thema [**Benutzer \_ Info \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) enthält eine Liste gültiger Werte für die Flags und eine Beschreibung der einzelnen Flags.


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a>Festlegen des vollständigen Benutzernamens, Ebene 1011

Das folgende Code Fragment veranschaulicht, wie der vollständige Name eines Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt wird. Das Thema [**Benutzer \_ Info \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) enthält weitere Informationen.


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 