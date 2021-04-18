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
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="cb7de-103">Ändern von Elementen von Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="cb7de-103">Changing Elements of User Information</span></span>

<span data-ttu-id="cb7de-104">Die Netzwerk Verwaltungsfunktionen stellen eine Vielzahl von Informationsebenen bereit, um das Ändern von Benutzerinformationen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="cb7de-105">Einige Ebenen erfordern Administratorrechte, um erfolgreich ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="cb7de-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="cb7de-106">Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="cb7de-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="cb7de-107">Der Beispielcode in diesem Thema veranschaulicht, wie mehrere Elemente von Benutzerinformationen durch Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cb7de-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-108">Der Code verwendet verschiedene Netzwerk Verwaltungs Informationsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="cb7de-109">Wenn Sie Benutzerinformationen ändern, empfiehlt es sich, eine bestimmte Ebene für diese Informationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb7de-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="cb7de-110">Dadurch wird verhindert, dass nicht verknüpfte Informationen versehentlich zurückgesetzt werden, wenn die Werte der niedrigeren Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb7de-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="cb7de-111">Das Festlegen einiger der häufig verwendeten Ebenen ist in den folgenden Codebeispielen dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cb7de-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="cb7de-112">Festlegen des Benutzer Kennworts, Ebene 1003</span><span class="sxs-lookup"><span data-stu-id="cb7de-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="cb7de-113">Festlegen der Benutzer Berechtigung, Ebene 1005</span><span class="sxs-lookup"><span data-stu-id="cb7de-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="cb7de-114">Festlegen des Basisverzeichnisses des Benutzers, Ebene 1006</span><span class="sxs-lookup"><span data-stu-id="cb7de-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="cb7de-115">Festlegen des Benutzer Kommentar Felds, Ebene 1007</span><span class="sxs-lookup"><span data-stu-id="cb7de-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="cb7de-116">Festlegen der Benutzerflags, Ebene 1008</span><span class="sxs-lookup"><span data-stu-id="cb7de-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="cb7de-117">Festlegen des Benutzer Skript Pfads, Ebene 1009</span><span class="sxs-lookup"><span data-stu-id="cb7de-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="cb7de-118">Festlegen der benutzerautorierungsflags, Ebene 1010</span><span class="sxs-lookup"><span data-stu-id="cb7de-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="cb7de-119">Festlegen des vollständigen Benutzernamens, Ebene 1011</span><span class="sxs-lookup"><span data-stu-id="cb7de-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="cb7de-120">Alle Code Fragmente gehen davon aus, dass der Benutzer die Unicode-Kompilierungs Direktive definiert und die entsprechenden SDK-Header Dateien wie folgt eingefügt hat:</span><span class="sxs-lookup"><span data-stu-id="cb7de-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


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



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="cb7de-121">Festlegen des Benutzer Kennworts, Ebene 1003</span><span class="sxs-lookup"><span data-stu-id="cb7de-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="cb7de-122">Das folgende Code Fragment veranschaulicht, wie das Kennwort eines Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " auf einen bekannten Wert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7de-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-123">Das Thema [**Benutzer \_ Info \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


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



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="cb7de-124">Festlegen der Benutzer Berechtigung, Ebene 1005</span><span class="sxs-lookup"><span data-stu-id="cb7de-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="cb7de-125">Das folgende Code Fragment veranschaulicht, wie die Ebene der Berechtigung, die einem Benutzer zugewiesen wird, mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb7de-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-126">Das Thema [**Benutzer \_ Info \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="cb7de-127">Weitere Informationen zu Konto Berechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges) und [Autorisierungs Konstanten](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="cb7de-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


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



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="cb7de-128">Festlegen des Basisverzeichnisses des Benutzers, Ebene 1006</span><span class="sxs-lookup"><span data-stu-id="cb7de-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="cb7de-129">Das folgende Code Fragment veranschaulicht, wie der Pfad des Basisverzeichnisses eines Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb7de-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-130">Bei dem Verzeichnis kann es sich um einen hart codierten Pfad oder um einen gültigen Unicode-Pfad handeln.</span><span class="sxs-lookup"><span data-stu-id="cb7de-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="cb7de-131">Das Thema [**Benutzer \_ Info \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


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



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="cb7de-132">Festlegen des Benutzer Kommentar Felds, Ebene 1007</span><span class="sxs-lookup"><span data-stu-id="cb7de-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="cb7de-133">Das folgende Code Fragment veranschaulicht, wie ein Kommentar einem Benutzer zugeordnet wird, indem die Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cb7de-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-134">Das Thema [**Benutzer \_ Info \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


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



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="cb7de-135">Festlegen der Benutzerflags, Ebene 1008</span><span class="sxs-lookup"><span data-stu-id="cb7de-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="cb7de-136">Das folgende Code Fragment veranschaulicht, wie Benutzerflags mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb7de-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-137">Das Thema [**Benutzer \_ Info \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) enthält eine Liste gültiger Werte für die Flags und eine Beschreibung der einzelnen Flags.</span><span class="sxs-lookup"><span data-stu-id="cb7de-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="cb7de-138">Beachten Sie, dass das \_ kennflag für das Angleichen Skript für Windows NT-, Windows 2000-, Windows XP-und LAN Manager-Netzwerke festgelegt werden muss</span><span class="sxs-lookup"><span data-stu-id="cb7de-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="cb7de-139">Wenn Sie versuchen, andere Flags festzulegen, ohne ein "UF- \_ Skript" auf diese Netzwerke festzulegen, schlägt die Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " fehl</span><span class="sxs-lookup"><span data-stu-id="cb7de-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


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



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="cb7de-140">Festlegen des Benutzer Skript Pfads, Ebene 1009</span><span class="sxs-lookup"><span data-stu-id="cb7de-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="cb7de-141">Das folgende Code Fragment veranschaulicht, wie der Pfad für die Anmelde Skriptdatei eines bestimmten Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7de-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-142">Die Skriptdatei kann ein sein. Cmd-Datei, eine. EXE-Datei oder ein. BAT-Datei.</span><span class="sxs-lookup"><span data-stu-id="cb7de-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="cb7de-143">Die Zeichenfolge kann auch NULL sein.</span><span class="sxs-lookup"><span data-stu-id="cb7de-143">The string can also be null.</span></span> <span data-ttu-id="cb7de-144">Das Thema [**Benutzer \_ Info \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


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



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="cb7de-145">Festlegen der benutzerautorierungsflags, Ebene 1010</span><span class="sxs-lookup"><span data-stu-id="cb7de-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="cb7de-146">Das folgende Code Fragment veranschaulicht, wie die Operatoren für Operator Privilegien für einen Benutzer mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb7de-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-147">Das Thema [**Benutzer \_ Info \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) enthält eine Liste gültiger Werte für die Flags und eine Beschreibung der einzelnen Flags.</span><span class="sxs-lookup"><span data-stu-id="cb7de-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


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



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="cb7de-148">Festlegen des vollständigen Benutzernamens, Ebene 1011</span><span class="sxs-lookup"><span data-stu-id="cb7de-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="cb7de-149">Das folgende Code Fragment veranschaulicht, wie der vollständige Name eines Benutzers mit einem Aufrufen der Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7de-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="cb7de-150">Das Thema [**Benutzer \_ Info \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cb7de-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


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



 

 