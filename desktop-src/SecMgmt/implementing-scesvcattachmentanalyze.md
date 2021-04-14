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
# <a name="implementing-scesvcattachmentanalyze"></a>Implementieren von scesvpetachmentanalysis

Die [**scesvasetachmentanalysis**](scesvcattachmentanalyze.md) -Funktion muss Konfigurationsinformationen aus der Sicherheitsdatenbank und dem Dienst abrufen, die beiden Informations Sätze vergleichen und dann den Analyse Abschnitt der Sicherheitsdatenbank mit Unterschieden aktualisieren. Dies können Sie mithilfe des folgenden Algorithmus sicherstellen.

**So implementieren Sie scesvpetachmentanalysis**

1.  Definieren Sie die Variablen, die zum Abrufen und Festlegen der Sicherheitsinformationen und Rückgabecodes erforderlich sind.
2.  Rufen Sie die pfqueryinfo-Rückruffunktion in der Rückruf Struktur auf, um Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.
3.  Rufen Sie die entsprechenden Informationen aus dem Dienst ab.
4.  Vergleichen Sie die Konfigurationsdaten, die vom-Dienst abgerufen werden, mit dem aus der Sicherheitsdatenbank abgerufenen.
5.  Wenn die Informationen nicht identisch sind, rufen Sie die Rückruffunktion pfabtinfo in der Rückruf Struktur auf, um die Datenbank zu aktualisieren.
6.  Freigeben aller Puffer, die zum Abrufen von Informationen verwendet werden. Rufen Sie die pffreeinfo-Rückruffunktion in der Rückruf Struktur auf, um Speicher freizugeben, der für die zurückgegebenen Datenbankinformationen
7.  Wenn eine Meldung vorhanden ist, die von der Erweiterung der Analyseprotokoll Datei hinzugefügt werden soll, rufen Sie die pfloginfo-Rückruffunktion in der Rückruf Struktur auf.
8.  Gibt die entsprechenden **scestatus** -Codes zurück.

Das folgende Beispiel zeigt eine mögliche Implementierung von [**scesvtortachmentanalysis**](scesvcattachmentanalyze.md). Beachten Sie, dass in diesem Beispiel die Funktionen "queryconfigurationline" und "CompareValue" Informationen vom Dienst Abfragen und diese Werte mit den Werten vergleichen, die von der Sicherheitsdatenbank abgerufen werden. Die Implementierung dieser Funktionen wird nicht angezeigt.


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



 

 



