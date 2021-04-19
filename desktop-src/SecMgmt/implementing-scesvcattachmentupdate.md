---
description: Nimmt als Parameter einen Satz von bereitgestellten Konfigurationsinformationen an.
ms.assetid: 3c0a71f6-f643-4a5e-8b5c-15c976a3736e
title: Implementieren von scesvertachmentupdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381a2b04b75399b5f580426d9f2dd9f5911f52d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360575"
---
# <a name="implementing-scesvcattachmentupdate"></a>Implementieren von scesvertachmentupdate

Die [**scesvgattachmentupdate**](scesvcattachmentupdate.md) -Funktion benötigt als Parameter einen Satz von bereitgestellten Konfigurationsinformationen. Anschließend werden Informationen aus der Sicherheitsdatenbank abgerufen, eine neue Basiskonfiguration mit den bereitgestellten Konfigurationsinformationen berechnet, neue Analyse Informationen auf der Grundlage der Datenbankinformationen und der angegebenen Konfigurationsinformationen berechnet und die Datenbank mit neuen grundlegenden Konfigurations-und Analyse Informationen aktualisiert. Sie können **scesvsintachmentupdate** mit dem folgenden Algorithmus implementieren.

**So implementieren Sie scesvertachmentupdate**

1.  Definieren Sie die Variablen, die zum Abrufen von Informationen, Festlegen von Informationen und Rückgabecodes erforderlich sind.
2.  Rufen Sie die pfqueryinfo-Rückruffunktion in der Rückruf Struktur auf, um die aktuellen Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.
3.  Vergleichen Sie die Werte:

    -   Wenn sich die Daten unterscheiden, rufen Sie die pfabtinfo-Rückruffunktion in der Rückruf Struktur auf, um die Konfigurationsdaten in der Datenbank zu aktualisieren.
    -   Wenn die Daten identisch sind, rufen Sie die pfsetinfo-Rückruffunktion in der Rückruf Struktur auf, um die Analysedaten in der Datenbank zu aktualisieren.

4.  Wiederholen Sie den Vorgang, bis alle Daten verarbeitet wurden.

Das folgende Beispiel zeigt eine mögliche Implementierung von [**scesvertachmentupdate**](scesvcattachmentupdate.md).


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo,
    IN SCESVC_CONFIGURATION_INFO *ServiceInfo
)
{
 
    ////////////////////////////////////////////////////
    // Define variables.
    ////////////////////////////////////////////////////
    SCESTATUS                      retCode;
    SCE_ENUMERATION_CONTEXT        EnumContext = 0;
    if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ||
         ServiceInfo == NULL ) 
    {
        return(SCESTATUS_INVALID_PARAMETER);
    }
  
  
    ////////////////////////////////////////////////////
    // Process supplied configuration information. 
    ////////////////////////////////////////////////////
    for (int i = 0; i < ServiceInfo->Count; i++)
    {
        retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              ServiceInfo->Line[I].Key,
                              TRUE,
                              (PVOID *)&pConfigInfo,
                              &EnumContext
                              );
        if(retCode != SCESTATUS_SUCCESS && 
           retCode != SCESTATUS_RECORD_NOT_FOUND)
        {
            ////////////////////////////////////////////////
            // Add code to handle errors
            ////////////////////////////////////////////////
            break;
        }
    
        //////////////////////////////////////////////////
        // If the supplied key is NULL, delete corresponding
        // key from configuration information and update 
        // analysis information if needed.
        //////////////////////////////////////////////////
        if(ServiceInfo->Line[I].Value == NULL)
        {
            if(retCode == SCESTATUS_SUCCESS)
            {
                EnumContext = 0;
                retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                          SceSvcAnalysisInfo,
                                          ServiceInfo->Line [i].Key,
                                          TRUE,
                                          (PVOID *)&pAnalInfo,
                                          &EnumContext
                                          );
                if(retCode == SCESTATUS_RECORD_NOT_FOUND)
                {
                  ////////////////////////////////////////////
                  // Analysis information for key was not found.
                  // Update analysis information to include 
                  // deleted key.
                  /////////////////////////////////////////////
                  UpdateInfo->Count = 1;
                  UpdateInfo->Line = &UpdateLine;
                  UpdateLine.Key = pConfigInfo->Line[0].Key;
                  UpdateLine.Value = (PBYTE)pConfigInfo->Line[0].Value;
                  retCode = (*(pSceCbInfo->pfSetInfo))( pSceCbInfo->sceHandle,
                                          SceSvcAnalysisInfo,
                                          NULL,
                                          TRUE,
                                          &UpdateInfo
                                          );
                  if(retCode != SCESTATUS_SUCCESS)
                  {
                    //////////////////////////////////////////
                    // Add code for error return codes.
                    //////////////////////////////////////////
                  } 
                }
                else if (retCode == SCESTATUS_SUCCESS)
                {
                 ////////////////////////////////////////////
                 // Add code to delete configuration (analysis
                 // information is already in place.
                 ////////////////////////////////////////////
                }
                else
                {
                  //////////////////////////////////////////
                  // Add code for error return codes.
                  //////////////////////////////////////////
                }
            
                //////////////////////////////////////////////
                // Delete key.
                //////////////////////////////////////////////
                retCode = (*(pSceCbInfo->pfSetInfo))( pSceCbInfo->sceHanlde,
                                        SceSvcConfigurationInfo,
                                        ServiceInfo->Line[I].Key,
                                        TRUE,
                                        NULL
                                        );
                if(retCode != SCESTATUS_SUCCESS)
                {
                  //////////////////////////////////////////
                  // Add code for error return codes.
                  //////////////////////////////////////////
                }
      
            }
            else
            {
                 /////////////////////////////////////////////////
                 // Supplied value is non-NULL; therefore. compare
                 // with current analysis information. If both are
                 // the same, delete current analysis. If they are 
                 // not the same, update security database with new
                 // value.
                 //////////////////////////////////////////
             
            }
   
   
           //////////////////////////////////////////////////
           // Free data returned.
           /////////////////////////////////////////////////
         (*(pSceCbInfo->pfFreeInfo))(pConfigInfo);
           pConfigInfo = NULL;
           
         (*(pSceCbInfo->pfSetInfo))(pAnalInfo);
           pAnalInfo = NULL;
          
          
          ////////////////////////////////////////////////////
          // Add code for other return codes if retCode is 
          // not SCESTATUS_SUCCESS.
          ///////////////////////////////////////////////////
          return retCode;
        }
    }
}
```



 

 



