---
description: 'Cryptography API: Next Generation (CNG) stellt Funktionen bereit, mit denen die Verschlüsselungs Sammlungen, die von einem Anbieter unterstützt werden, abgefragt, hinzugefügt, entfernt und priorisiert werden. Mit diesen Funktionen vorgenommene Änderungen werden sofort wirksam, und es ist nicht erforderlich, einen aktiven Server neu zu starten.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Priorisieren von SChannel-Verschlüsselungs Sammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219071"
---
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="14eb1-104">Priorisieren von SChannel-Verschlüsselungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="14eb1-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="14eb1-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) stellt Funktionen bereit, mit denen die Verschlüsselungs Sammlungen, die von einem Anbieter unterstützt werden, abgefragt, hinzugefügt, entfernt und priorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="14eb1-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="14eb1-106">Mit diesen Funktionen vorgenommene Änderungen werden sofort wirksam, und es ist nicht erforderlich, einen aktiven Server neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="14eb1-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="14eb1-107">Sie können auch die Liste der Verschlüsselungs Sammlungen ändern, indem Sie die Gruppenrichtlinien Einstellungen für die Verschlüsselung der SSL-Verschlüsselungs **Sammlung** mithilfe des Snap-Ins "Gruppenrichtlinie-Objekt" in der Microsoft Management Console konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="14eb1-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="14eb1-108">**So konfigurieren Sie die Gruppenrichtlinien Einstellung "SSL-Verschlüsselungs **Sammlung** "**</span><span class="sxs-lookup"><span data-stu-id="14eb1-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="14eb1-109">Geben Sie an einer Eingabeaufforderung **gpeer dit. msc** ein.</span><span class="sxs-lookup"><span data-stu-id="14eb1-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="14eb1-110">Der **Gruppenrichtlinienobjekt-Editor** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14eb1-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="14eb1-111">Erweitern Sie **Computer Konfiguration**, **Administrative Vorlagen** und **Netzwerk**, und klicken Sie dann auf **SSL-Konfigurationseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="14eb1-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="14eb1-112">Klicken Sie unter **SSL-Konfigurationseinstellungen** auf die Einstellung für die **Reihenfolge der SSL** -Verschlüsselungs Sammlungen.</span><span class="sxs-lookup"><span data-stu-id="14eb1-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="14eb1-113">Scrollen Sie im Bereich für die **Reihenfolge der SSL** -Verschlüsselungs Sammlungen zum unteren Rand des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="14eb1-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="14eb1-114">Befolgen Sie die Anweisungen **zum Ändern dieser Einstellung**.</span><span class="sxs-lookup"><span data-stu-id="14eb1-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="14eb1-115">Sie müssen den Computer neu starten, nachdem Sie diese Einstellung geändert haben, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="14eb1-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="14eb1-116">Die Liste der Verschlüsselungs Sammlungen ist auf 1023 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="14eb1-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="14eb1-117">Informationen zum Priorisieren von SChannel-Verschlüsselungs Sammlungen finden Sie in den folgenden Beispielen.</span><span class="sxs-lookup"><span data-stu-id="14eb1-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="14eb1-118">Auflisten unterstützter Verschlüsselungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="14eb1-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="14eb1-119">Hinzufügen, entfernen und Priorisieren von Verschlüsselungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="14eb1-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="14eb1-120">Auflisten unterstützter Verschlüsselungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="14eb1-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="14eb1-121">Aufrufen der Funktion " [**bcryptenumschlag**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) " zum Auflisten der Verschlüsselungs Sammlungen, die von einem Anbieter in der Reihenfolge ihrer Priorität unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="14eb1-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="14eb1-122">Im folgenden Beispiel wird veranschaulicht, wie mit der Funktion " [**bcryptenumschlag**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) " unterstützte Verschlüsselungs Sammlungen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="14eb1-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="14eb1-123">Hinzufügen, entfernen und Priorisieren von Verschlüsselungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="14eb1-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="14eb1-124">Aufrufen der Funktionen [**bcryptaddcontextfunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) und [**bcryptremuvecontextfunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) zum Hinzufügen und Entfernen von Verschlüsselungs Sammlungen aus der Liste der unterstützten Verschlüsselungs Sammlungen.</span><span class="sxs-lookup"><span data-stu-id="14eb1-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="14eb1-125">Legen Sie beim Hinzufügen einer Verschlüsselungs Sammlung den Wert des *dwposition* -Parameters der Funktion " [**bcryptaddcontextfunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) " auf " **crypt \_ Priorität \_ oben** " fest, um ihn am Anfang der priorisierten Liste hinzuzufügen, oder auf die nach-oben- **\_ \_ Seite** , um ihn am Ende der Liste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="14eb1-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="14eb1-126">Um die Liste der Verschlüsselungs Sammlungen zu priorisieren, entfernen Sie alle Verschlüsselungs Sammlungen aus der Liste, und fügen Sie der Liste anschließend Verschlüsselungs Sammlungen in der gewünschten Reihenfolge hinzu.</span><span class="sxs-lookup"><span data-stu-id="14eb1-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="14eb1-127">Im folgenden Beispiel wird gezeigt, wie eine Verschlüsselungs Sammlung am Anfang der priorisierten Liste für den standardmäßigen Microsoft SChannel-Anbieter hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="14eb1-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



<span data-ttu-id="14eb1-128">Im folgenden Beispiel wird gezeigt, wie eine Verschlüsselungs Sammlung aus der priorisierten Liste für den standardmäßigen Microsoft SChannel-Anbieter entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="14eb1-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
