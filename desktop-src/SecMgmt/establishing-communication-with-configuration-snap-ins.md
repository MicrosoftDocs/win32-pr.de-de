---
description: Nachdem die Erweiterungs-Snap-in-Erweiterung dem Knoten Dienste hinzugefügt wurde, sollte Sie die Kommunikation mit dem Snap-in für die Sicherheitskonfiguration herstellen.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Einrichten der Kommunikation mit Konfigurations-Snap-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363254"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>Einrichten der Kommunikation mit Konfigurations-Snap-Ins

Nachdem die Erweiterungs-Snap-in-Erweiterung dem Knoten Dienste hinzugefügt wurde, sollte Sie die Kommunikation mit dem Snap-in für die Sicherheitskonfiguration herstellen. Dies ist erforderlich, da die Erweiterungs-Snap-in-Erweiterung sowohl Ihre Daten als auch alle vom Benutzer vorgenommenen Änderungen über das Sicherheitskonfigurations-Snap-in abruft. Dies kann wie im folgenden Verfahren beschrieben erfolgen.

**So richten Sie die Kommunikation mit den Snap-Ins für die Sicherheitskonfiguration ein**

1.  Rufen Sie den Konfigurations Dateinamen mit dem CCF \_ scesvc- \_ Zwischenablage Format ab, das den Konfigurations Dateinamen als **pwstr** zurückgibt.

    Wenn die Anlage unter einem Knotentyp Knoten eingefügt wird, muss die anlagewissen, welche Konfiguration Sie ist. (Er kommuniziert diese Informationen an die Sicherheitskonfigurations-Snap-Ins während der Schnittstellen Initialisierung.) Verwenden Sie in diesem Fall den folgenden Code.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Richten Sie den Kontext mit den Snap-Ins für die Sicherheitskonfiguration ein. Nachdem der Konfigurations Name bekannt ist oder der Dienst Knoten ein Analyse Knoten ist, muss die Erweiterungs-Snap-in-Erweiterung [**iscesvasetachmentdata:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) anrufen, um den Kontext einzurichten, wie im folgenden Beispiel gezeigt.

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> Wenn Sie das von [**iscesvcalltachmentdata:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize)zurückgegebene Handle nicht mehr verwenden, schließen Sie das Handle, indem Sie die [**iscesvcalltachmentdata:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) -Funktion aufrufen. Dies erfolgt in der Regel, wenn der Benutzer die MMC-Konsole schließt.

 

 

 



