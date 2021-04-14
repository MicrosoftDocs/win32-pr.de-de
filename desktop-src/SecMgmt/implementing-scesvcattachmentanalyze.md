---
description: Muss Konfigurationsinformationen aus der Sicherheitsdatenbank und dem Dienst abrufen, die beiden Informations Sätze vergleichen und dann den Analyse Abschnitt der Sicherheitsdatenbank mit Unterschieden aktualisieren.
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: Implementieren von scesvpetachmentanalysis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217149"
---
# <a name="implementing-scesvcattachmentanalyze"></a><span data-ttu-id="2b080-103">Implementieren von scesvpetachmentanalysis</span><span class="sxs-lookup"><span data-stu-id="2b080-103">Implementing SceSvcAttachmentAnalyze</span></span>

<span data-ttu-id="2b080-104">Die [**scesvasetachmentanalysis**](scesvcattachmentanalyze.md) -Funktion muss Konfigurationsinformationen aus der Sicherheitsdatenbank und dem Dienst abrufen, die beiden Informations Sätze vergleichen und dann den Analyse Abschnitt der Sicherheitsdatenbank mit Unterschieden aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2b080-104">The [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) function must retrieve configuration information from the security database and the service, compare the two sets of information, and then update the analysis section of the security database with any differences.</span></span> <span data-ttu-id="2b080-105">Dies können Sie mithilfe des folgenden Algorithmus sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="2b080-105">You can ensure this by using the following algorithm.</span></span>

<span data-ttu-id="2b080-106">**So implementieren Sie scesvpetachmentanalysis**</span><span class="sxs-lookup"><span data-stu-id="2b080-106">**To implement SceSvcAttachmentAnalyze**</span></span>

1.  <span data-ttu-id="2b080-107">Definieren Sie die Variablen, die zum Abrufen und Festlegen der Sicherheitsinformationen und Rückgabecodes erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2b080-107">Define the variables needed to retrieve and set the security information and return codes.</span></span>
2.  <span data-ttu-id="2b080-108">Rufen Sie die pfqueryinfo-Rückruffunktion in der Rückruf Struktur auf, um Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b080-108">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="2b080-109">Rufen Sie die entsprechenden Informationen aus dem Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="2b080-109">Retrieve the corresponding information from the service.</span></span>
4.  <span data-ttu-id="2b080-110">Vergleichen Sie die Konfigurationsdaten, die vom-Dienst abgerufen werden, mit dem aus der Sicherheitsdatenbank abgerufenen.</span><span class="sxs-lookup"><span data-stu-id="2b080-110">Compare the configuration data retrieved from the service with that retrieved from the security database.</span></span>
5.  <span data-ttu-id="2b080-111">Wenn die Informationen nicht identisch sind, rufen Sie die Rückruffunktion pfabtinfo in der Rückruf Struktur auf, um die Datenbank zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2b080-111">If the information is not the same, call the pfSetInfo callback function in the callback structure to update the database.</span></span>
6.  <span data-ttu-id="2b080-112">Freigeben aller Puffer, die zum Abrufen von Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b080-112">Free all buffers used to retrieve information.</span></span> <span data-ttu-id="2b080-113">Rufen Sie die pffreeinfo-Rückruffunktion in der Rückruf Struktur auf, um Speicher freizugeben, der für die zurückgegebenen Datenbankinformationen</span><span class="sxs-lookup"><span data-stu-id="2b080-113">Call the pfFreeInfo callback function in the callback structure to free memory used for returned database information.</span></span>
7.  <span data-ttu-id="2b080-114">Wenn eine Meldung vorhanden ist, die von der Erweiterung der Analyseprotokoll Datei hinzugefügt werden soll, rufen Sie die pfloginfo-Rückruffunktion in der Rückruf Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="2b080-114">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
8.  <span data-ttu-id="2b080-115">Gibt die entsprechenden **scestatus** -Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="2b080-115">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="2b080-116">Das folgende Beispiel zeigt eine mögliche Implementierung von [**scesvtortachmentanalysis**](scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="2b080-116">The following example shows one possible implementation of [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span></span> <span data-ttu-id="2b080-117">Beachten Sie, dass in diesem Beispiel die Funktionen "queryconfigurationline" und "CompareValue" Informationen vom Dienst Abfragen und diese Werte mit den Werten vergleichen, die von der Sicherheitsdatenbank abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2b080-117">Note that in this example, the functions QueryConfigurationLine and CompareValue respectively query information from the service and compare those values with those retrieved from the security database.</span></span> <span data-ttu-id="2b080-118">Die Implementierung dieser Funktionen wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2b080-118">The implementation of these functions is not shown.</span></span>


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
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
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



