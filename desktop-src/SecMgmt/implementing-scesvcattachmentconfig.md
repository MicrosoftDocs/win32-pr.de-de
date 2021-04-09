---
description: Muss Informationen aus der Sicherheitsdatenbank abrufen und diese Informationen dann verwenden, um den Dienst zu konfigurieren.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Implementieren von scesvalisitachmentconfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960255"
---
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="76019-103">Implementieren von scesvalisitachmentconfig</span><span class="sxs-lookup"><span data-stu-id="76019-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="76019-104">Die [**scesvstreamtachmentconfig**](scesvcattachmentconfig.md) -Funktion muss Informationen aus der Sicherheitsdatenbank abrufen und diese Informationen dann verwenden, um den Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="76019-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="76019-105">Bei der Implementierung von [**scesvsintachmentconfig**](scesvcattachmentconfig.md)können Sie entweder alle Informationen abrufen und dann den Dienst konfigurieren oder den Dienst in den Schritten abrufen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="76019-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="76019-106">Der folgende Algorithmus Ruft alle Informationen ab und konfiguriert dann den Dienst.</span><span class="sxs-lookup"><span data-stu-id="76019-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="76019-107">**So implementieren Sie scesvalisitachmentconfig**</span><span class="sxs-lookup"><span data-stu-id="76019-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="76019-108">Definieren Sie die Variablen, die zum Abrufen von Informationen und Rückgabecodes erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="76019-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="76019-109">Rufen Sie die pfqueryinfo-Rückruffunktion in der Rückruf Struktur auf, um Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76019-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="76019-110">Konfigurieren Sie das System mit den zurückgegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="76019-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="76019-111">Rufen Sie die pffreeinfo-Rückruffunktion in der Rückruf Struktur auf, um den für zurückgegebene Informationen verwendeten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="76019-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="76019-112">Wenn eine Meldung vorhanden ist, die von der Erweiterung der Analyseprotokoll Datei hinzugefügt werden soll, rufen Sie die pfloginfo-Rückruffunktion in der Rückruf Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="76019-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="76019-113">Gibt die entsprechenden **scestatus** -Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="76019-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="76019-114">Das folgende Beispiel zeigt eine mögliche Implementierung von [**scesvtortachmentconfig**](scesvcattachmentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="76019-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="76019-115">Beachten Sie, dass in diesem Beispiel die-Funktion processconfigurationline die Dienst Konfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="76019-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="76019-116">Die Implementierung dieser Funktion wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76019-116">The implementation of this function is not shown.</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
  ////////////////////////////////////////////////////
  // Define variables.
  ////////////////////////////////////////////////////
     PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
     SCESTATUS                      retCode;
     SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
     if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
     {
        return(SCESTATUS_INVALID_PARAMETER);
     }
  
  
      ////////////////////////////////////////////////////
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



