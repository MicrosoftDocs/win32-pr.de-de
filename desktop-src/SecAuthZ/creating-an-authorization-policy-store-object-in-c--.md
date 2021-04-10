---
description: Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959215"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++

Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind. Wenn eine Anwendung, die den Autorisierungs-Manager verwendet, initialisiert, lädt Sie diese Informationen aus dem Speicher. Der Autorisierungs Richtlinien Speicher muss sich in einem vertrauenswürdigen System befinden, da Administratoren auf diesem System über ein hohes Maß an Zugriff auf den Store verfügen.

Der Autorisierungs-Manager unterstützt das Speichern von Autorisierungs Richtlinien entweder im Active Directory Directory-Dienst oder in einer XML-Datei, wie in den folgenden Beispielen gezeigt. In der Autorisierungs-Manager-API wird ein Autorisierungs Richtlinien Speicher durch ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt dargestellt. In den Beispielen wird gezeigt, wie ein **AzAuthorizationStore** -Objekt für einen Active Directory-Speicher und einen XML-Speicher erstellt wird.

-   [Erstellen eines Active Directory Stores](#creating-an-active-directory-store)
-   [Erstellen eines SQL Server Stores](#creating-a-sql-server-store)
-   [Erstellen eines XML-Stores](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Erstellen eines Active Directory Stores

Um Active Directory zum Speichern der Autorisierungs Richtlinie zu verwenden, muss sich die Domäne auf der **Windows Server 2003** -Domänen Funktionsebene befinden. Der Autorisierungs Richtlinien Speicher kann nicht in einem **nicht-Domänen-namens Kontext** (auch als Anwendungs Partition bezeichnet) gefunden werden. Es wird empfohlen, dass sich der Speicher im **Programm Daten** Container unter einer neuen Organisationseinheit befindet, die speziell für den Autorisierungs Richtlinien Speicher erstellt wurde. Außerdem wird empfohlen, dass sich der Speicher innerhalb desselben lokalen Netzwerks befindet wie Anwendungsserver, die Anwendungen ausführen, die den Speicher verwenden.

Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in Active Directory darstellt. In diesem Beispiel wird davon ausgegangen, dass in einer Domäne mit dem Namen AuthManager.com eine vorhandene Organisationseinheit mit dem Namen Program Data Active Directory vorhanden ist.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



## <a name="creating-a-sql-server-store"></a>Erstellen eines SQL Server Stores

Der Autorisierungs-Manager unterstützt das Erstellen eines Microsoft SQL Server – basierten Autorisierungs Richtlinien Speicher. Um einen SQL Server – basierten Autorisierungs Speicher zu erstellen, verwenden Sie eine URL, die mit dem Präfix **MSSQL://** beginnt. Die URL muss eine gültige SQL-Verbindungs Zeichenfolge, einen Datenbanknamen und den Namen des Autorisierungs Richtlinien Speicher enthalten: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _policystorename_.

Wenn die Instanz von SQL Server die angegebene Autorisierungs-Manager-Datenbank nicht enthält, erstellt der Autorisierungs-Manager eine neue Datenbank mit diesem Namen.

> [!Note]  
> Verbindungen mit einem SQL Server Speicher werden nur dann verschlüsselt, wenn Sie die SQL-Verschlüsselung für die Verbindung explizit einrichten oder die Verschlüsselung des Netzwerk Datenverkehrs einrichten, der IPSec (Internet Protocol Security) verwendet.

 

Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer SQL Server-Datenbank darstellt.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



## <a name="creating-an-xml-store"></a>Erstellen eines XML-Stores

Der Autorisierungs-Manager unterstützt das Erstellen eines Autorisierungs Richtlinien Speicher im XML-Format Der XML-Speicher kann sich auf demselben Computer befinden, auf dem die Anwendung ausgeführt wird, oder er kann Remote gespeichert werden. Das direkte Bearbeiten der XML-Datei wird nicht unterstützt. Verwenden Sie das Autorisierungs-Manager-MMC-Snap-in oder die Autorisierungs-Manager-API zum Bearbeiten des Richtlinien Speicher.

Der Autorisierungs-Manager unterstützt nicht die Delegierung der Verwaltung eines XML-Richtlinien Speicher. Weitere Informationen zur Delegierung finden Sie unter [Delegieren der Definition von Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md).

Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer XML-Datei darstellt.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



