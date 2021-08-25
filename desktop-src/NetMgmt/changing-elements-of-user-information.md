---
title: Ändern von Elementen von Benutzerinformationen
description: Die Netzwerkverwaltungsfunktionen bieten eine Vielzahl von Informationsebenen zur Unterstützung beim Ändern von Benutzerinformationen.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3161bb4d689b70f85f6c20c7c302779d0f685e8bcace43cffdee68b2cda2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912500"
---
# <a name="changing-elements-of-user-information"></a>Ändern von Elementen von Benutzerinformationen

Die Netzwerkverwaltungsfunktionen bieten eine Vielzahl von Informationsebenen zur Unterstützung beim Ändern von Benutzerinformationen. Einige Ebenen erfordern Administratorrechte, um erfolgreich ausgeführt zu werden. Weitere Informationen zum Aufrufen von Funktionen, die Administratorrechte erfordern, finden Sie unter [Ausführen mit speziellen Berechtigungen.](/windows/desktop/SecBP/running-with-special-privileges)

Der Beispielcode in diesem Thema veranschaulicht, wie mehrere Elemente von Benutzerinformationen durch Aufrufen der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) geändert werden. Der Code verwendet verschiedene Netzwerkverwaltungsinformationsstrukturen.

Beim Ändern von Benutzerinformationen empfiehlt es sich, die spezifische Ebene für diese Information zu verwenden. Dadurch wird verhindert, dass nicht verknüpfte Informationen versehentlich zurückgesetzt werden, wenn die niedrigeren Ebenenwerte verwendet werden.

Das Festlegen einiger der am häufigsten verwendeten Ebenen wird in den folgenden Codebeispielen veranschaulicht:

-   [Festlegen des Benutzerkennworts, Ebene 1003](#setting-the-user-password-level-1003)
-   [Festlegen der Benutzerberechtigung, Ebene 1005](#setting-the-user-privilege-level-1005)
-   [Festlegen des Benutzer-Stammverzeichnisses, Ebene 1006](#setting-the-user-home-directory-level-1006)
-   [Festlegen des Felds "Benutzerkommentar", Ebene 1007](#setting-the-user-comment-field-level-1007)
-   [Festlegen der Benutzerflags, Ebene 1008](#setting-the-user-flags-level-1008)
-   [Festlegen des Benutzerskriptpfads, Ebene 1009](#setting-the-user-script-path-level-1009)
-   [Festlegen der Benutzerautoritätsflags, Ebene 1010](#setting-the-user-authority-flags-level-1010)
-   [Festlegen des vollständigen Benutzernamens, Ebene 1011](#setting-the-user-full-name-level-1011)

Alle Codefragmente gehen davon aus, dass der Benutzer die UNICODE-Kompilierungsdirektive definiert und die entsprechenden SDK-Headerdateien wie folgt eingeschlossen hat:


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



## <a name="setting-the-user-password-level-1003"></a>Festlegen des Benutzerkennworts, Ebene 1003

Das folgende Codefragment veranschaulicht, wie das Kennwort eines Benutzers mit einem Aufruf der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) auf einen bekannten Wert festgelegt wird. Das Thema [**USER \_ INFO \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) enthält zusätzliche Informationen.


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



## <a name="setting-the-user-privilege-level-1005"></a>Festlegen der Benutzerberechtigung, Ebene 1005

Das folgende Codefragment veranschaulicht, wie sie die Einem Benutzer zugewiesene Berechtigungsebene mit einem Aufruf der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) angeben. Das Thema [**USER \_ INFO \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) enthält zusätzliche Informationen. Weitere Informationen zu Kontoberechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges) und [Autorisierungskonstanten.](/windows/desktop/SecAuthZ/authorization-constants)


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



## <a name="setting-the-user-home-directory-level-1006"></a>Festlegen des Benutzer-Stammverzeichnisses, Ebene 1006

Das folgende Codefragment veranschaulicht, wie der Pfad des Stammverzeichnisses eines Benutzers mit einem Aufruf der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) angegeben wird. Bei dem Verzeichnis kann es sich um einen hart codierten Pfad oder einen gültigen Unicode-Pfad handeln. Das Thema [**USER \_ INFO \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) enthält zusätzliche Informationen.


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



## <a name="setting-the-user-comment-field-level-1007"></a>Festlegen des Felds "Benutzerkommentar", Ebene 1007

Das folgende Codefragment veranschaulicht das Zuordnen eines Kommentars zu einem Benutzer durch Aufrufen der [**NetUserSetInfo-Funktion.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) Das Thema [**USER \_ INFO \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) enthält zusätzliche Informationen.


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

Das folgende Codefragment veranschaulicht das Festlegen von Benutzerflags mit einem Aufruf der [**NetUserSetInfo-Funktion.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) Das Thema [**USER \_ INFO \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) enthält eine Liste gültiger Werte für die Flags und eine Beschreibung der einzelnen Flags.

Beachten Sie, dass das UF \_ SCRIPT-Flag für Windows NT-, Windows 2000-, Windows XP- und LAN Manager-Netzwerke festgelegt werden muss. Der Versuch, andere Flags festzulegen, ohne UF SCRIPT in diesen Netzwerken festzulegen, \_ führt dazu, dass die [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) fehlschlägt.


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



## <a name="setting-the-user-script-path-level-1009"></a>Festlegen des Benutzerskriptpfads, Ebene 1009

Das folgende Codefragment veranschaulicht, wie der Pfad für die Anmeldeskriptdatei eines bestimmten Benutzers mit einem Aufruf der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) festgelegt wird. Die Skriptdatei kann ein sein. CMD-Datei, .EXE- oder .BAT datei. Die Zeichenfolge kann auch NULL sein. Das Thema [**USER \_ INFO \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) enthält zusätzliche Informationen.


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



## <a name="setting-the-user-authority-flags-level-1010"></a>Festlegen der Benutzerautoritätsflags, Ebene 1010

Das folgende Codefragment veranschaulicht, wie die Operatorberechtigungsflags für einen Benutzer mit einem Aufruf der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) festgelegt werden. Das Thema [**USER \_ INFO \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) enthält eine Liste gültiger Werte für die Flags und eine Beschreibung der einzelnen Flags.


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

Das folgende Codefragment veranschaulicht, wie der vollständige Name eines Benutzers mit einem Aufruf der [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) festgelegt wird. Das Thema [**USER \_ INFO \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) enthält zusätzliche Informationen.


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



 

 