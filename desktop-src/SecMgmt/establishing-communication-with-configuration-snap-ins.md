---
description: Nachdem sich ihre Snap-In-Erweiterung für Anlagen dem Knoten Dienste hinzugefügt hat, sollte sie eine Kommunikation mit dem Sicherheitskonfigurations-Snap-In herstellen.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Einrichten der Kommunikation mit Konfigurations-Snap-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf186936f0b0ad21dc871a91e78dd0bbead04a0683450992e5e3b7dd7c516abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969398"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>Einrichten der Kommunikation mit Konfigurations-Snap-Ins

Nachdem sich ihre Snap-In-Erweiterung für Anlagen dem Knoten Dienste hinzugefügt hat, sollte sie eine Kommunikation mit dem Sicherheitskonfigurations-Snap-In herstellen. Dies ist erforderlich, da die Snap-In-Erweiterung für Anlagen seine Daten sowie alle vom Benutzer vorgenommenen Änderungen aus dem Sicherheitskonfigurations-Snap-In erhält. Dies kann wie im folgenden Verfahren beschrieben erfolgen.

**So richten Sie die Kommunikation mit den Sicherheitskonfigurations-Snap-Ins ein**

1.  Abrufen des Konfigurationsdateinamens mithilfe des CCF SCESVC ATTACHMENT-Zwischenablageformats, das den Konfigurationsdateinamen \_ \_ als **PWSTR zurückgibt.**

    Wenn die Anlage unter einem Konfigurationstypknoten eingefügt wird, muss die Anlage wissen, um welche Konfiguration es sich handelt. (Diese Informationen werden während der Schnittstellenin initialisierung an die Sicherheitskonfigurations-Snap-Ins übermittelt.) Verwenden Sie in diesem Fall den folgenden Code.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Richten Sie den Kontext mit den Sicherheitskonfigurations-Snap-Ins ein. Nachdem der Konfigurationsname bekannt ist oder der Dienstknoten ein Analyseknoten ist, muss die Snap-In-Erweiterung für Anlagen [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) aufrufen, um den Kontext wie im folgenden Beispiel zu konfigurieren.

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
> Wenn Sie das von [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize)zurückgegebene Handle nicht mehr verwenden, schließen Sie das Handle, indem Sie die [**ISceSvcAttachmentData::CloseHandle-Funktion**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) aufrufen. Dies erfolgt in der Regel, wenn der Benutzer die MMC-Konsole schließt.

 

 

 



