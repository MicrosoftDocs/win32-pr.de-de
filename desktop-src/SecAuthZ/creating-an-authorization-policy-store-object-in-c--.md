---
description: Ein Autorisierungsrichtlinienspeicher enthält Informationen zur Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Die Informationen umfassen die Anwendungen, Vorgänge, Aufgaben, Benutzer und Benutzergruppen, die dem Speicher zugeordnet sind.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Erstellen einer Autorisierungsrichtlinie Store-Objekts in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be0b39633eb773b84ad16098f24b59cb23e5d9cc234afdfca414e9cba7a640b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782465"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Erstellen einer Autorisierungsrichtlinie Store-Objekts in C++

Ein Autorisierungsrichtlinienspeicher enthält Informationen zur Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Die Informationen umfassen die Anwendungen, Vorgänge, Aufgaben, Benutzer und Benutzergruppen, die dem Speicher zugeordnet sind. Wenn eine Anwendung, die den Autorisierungs-Manager verwendet, initialisiert wird, lädt sie diese Informationen aus dem Speicher. Der Autorisierungsrichtlinienspeicher muss sich auf einem vertrauenswürdigen System befinden, da Administratoren auf diesem System einen hohen Zugriff auf den Speicher haben.

Autorisierungs-Manager unterstützt das Speichern von Autorisierungsrichtlinien im Active Directory-Verzeichnisdienst oder in einer XML-Datei, wie in den folgenden Beispielen gezeigt. In der Autorisierungs-Manager-API wird ein Autorisierungsrichtlinienspeicher durch ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) dargestellt. Die Beispiele zeigen, wie ein **AzAuthorizationStore-Objekt** für einen Active Directory-Speicher und einen XML-Speicher erstellt wird.

-   [Erstellen eines Active Directory-Store](#creating-an-active-directory-store)
-   [Erstellen eines SQL Server Store](#creating-a-sql-server-store)
-   [Erstellen eines XML-Store](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Erstellen eines Active Directory-Store

Um Active Directory zum Speichern der Autorisierungsrichtlinie zu verwenden, muss sich die Domäne auf der **Domänenfunktionsebene Windows Server 2003** befinden. Der Autorisierungsrichtlinienspeicher kann sich nicht in einem **Nichtdomänenbenennungskontext** (auch als Anwendungspartition bezeichnet) befinden. Es wird empfohlen, dass sich der Speicher im **Container Programmdaten** in einer neuen Organisationseinheit befindet, die speziell für den Autorisierungsrichtlinienspeicher erstellt wurde. Es wird auch empfohlen, dass sich der Speicher im selben lokalen Netzwerk wie Anwendungsserver befindet, auf denen Anwendungen ausgeführt werden, die den Speicher verwenden.

Das folgende Beispiel zeigt, wie Sie ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) erstellen, das einen Autorisierungsrichtlinienspeicher in Active Directory darstellt. Im Beispiel wird davon ausgegangen, dass eine vorhandene Active Directory-Organisationseinheit namens Program Data in einer Domäne mit dem Namen authmanager.com vorhanden ist.


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



## <a name="creating-a-sql-server-store"></a>Erstellen eines SQL Server Store

Der Autorisierungs-Manager unterstützt das Erstellen eines Microsoft SQL Server basierten Autorisierungsrichtlinienspeichers. Um einen SQL Server basierten Autorisierungsspeicher zu erstellen, verwenden Sie eine URL, die mit dem Präfix **MSSQL://** beginnt. Die URL muss eine gültige SQL Verbindungszeichenfolge, einen Datenbanknamen und den Namen des Autorisierungsrichtlinienspeichers enthalten: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Wenn die Instanz von SQL Server nicht die angegebene Authorization Manager-Datenbank enthält, erstellt der Autorisierungs-Manager eine neue Datenbank mit diesem Namen.

> [!Note]  
> Verbindungen mit einem SQL Server Speicher werden nicht verschlüsselt, es sei denn, Sie richten explizit SQL Verschlüsselung für die Verbindung ein oder richten die Verschlüsselung des Netzwerkdatenverkehrs ein, der Internetprotokollsicherheit (Internet Protocol Security, IPsec) verwendet.

 

Das folgende Beispiel zeigt, wie Sie ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) erstellen, das einen Autorisierungsrichtlinienspeicher in einer SQL Server Datenbank darstellt.


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



## <a name="creating-an-xml-store"></a>Erstellen eines XML-Store

Der Autorisierungs-Manager unterstützt das Erstellen eines Autorisierungsrichtlinienspeichers im XML-Format. Der XML-Speicher kann sich auf demselben Computer befinden, auf dem die Anwendung ausgeführt wird, oder er kann remote gespeichert werden. Das direkte Bearbeiten der XML-Datei wird nicht unterstützt. Verwenden Sie das MMC-Snap-In für den Autorisierungs-Manager oder die Autorisierungs-Manager-API, um den Richtlinienspeicher zu bearbeiten.

Der Autorisierungs-Manager unterstützt nicht das Delegieren der Verwaltung eines XML-Richtlinienspeichers. Informationen zur Delegierung finden Sie unter [Delegieren der Definition von Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md).

Das folgende Beispiel zeigt, wie Sie ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) erstellen, das einen Autorisierungsrichtlinienspeicher in einer XML-Datei darstellt.


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



 

 



