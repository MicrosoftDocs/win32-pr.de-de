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
# <a name="implementing-scesvcattachmentconfig"></a>Implementieren von scesvalisitachmentconfig

Die [**scesvstreamtachmentconfig**](scesvcattachmentconfig.md) -Funktion muss Informationen aus der Sicherheitsdatenbank abrufen und diese Informationen dann verwenden, um den Dienst zu konfigurieren.

Bei der Implementierung von [**scesvsintachmentconfig**](scesvcattachmentconfig.md)können Sie entweder alle Informationen abrufen und dann den Dienst konfigurieren oder den Dienst in den Schritten abrufen und konfigurieren. Der folgende Algorithmus Ruft alle Informationen ab und konfiguriert dann den Dienst.

**So implementieren Sie scesvalisitachmentconfig**

1.  Definieren Sie die Variablen, die zum Abrufen von Informationen und Rückgabecodes erforderlich sind.
2.  Rufen Sie die pfqueryinfo-Rückruffunktion in der Rückruf Struktur auf, um Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.
3.  Konfigurieren Sie das System mit den zurückgegebenen Informationen.
4.  Rufen Sie die pffreeinfo-Rückruffunktion in der Rückruf Struktur auf, um den für zurückgegebene Informationen verwendeten Arbeitsspeicher freizugeben.
5.  Wenn eine Meldung vorhanden ist, die von der Erweiterung der Analyseprotokoll Datei hinzugefügt werden soll, rufen Sie die pfloginfo-Rückruffunktion in der Rückruf Struktur auf.
6.  Gibt die entsprechenden **scestatus** -Codes zurück.

Das folgende Beispiel zeigt eine mögliche Implementierung von [**scesvtortachmentconfig**](scesvcattachmentconfig.md). Beachten Sie, dass in diesem Beispiel die-Funktion processconfigurationline die Dienst Konfiguration festlegt. Die Implementierung dieser Funktion wird nicht angezeigt.


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



 

 



