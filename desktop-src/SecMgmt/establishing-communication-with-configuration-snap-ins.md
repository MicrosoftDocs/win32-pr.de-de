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
# <a name="establishing-communication-with-configuration-snap-ins"></a><span data-ttu-id="f7436-103">Einrichten der Kommunikation mit Konfigurations-Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="f7436-103">Establishing Communication with Configuration Snap-ins</span></span>

<span data-ttu-id="f7436-104">Nachdem die Erweiterungs-Snap-in-Erweiterung dem Knoten Dienste hinzugefügt wurde, sollte Sie die Kommunikation mit dem Snap-in für die Sicherheitskonfiguration herstellen.</span><span class="sxs-lookup"><span data-stu-id="f7436-104">After your attachment snap-in extension has added itself to the Services node, it should establish communication with the Security Configuration snap-in.</span></span> <span data-ttu-id="f7436-105">Dies ist erforderlich, da die Erweiterungs-Snap-in-Erweiterung sowohl Ihre Daten als auch alle vom Benutzer vorgenommenen Änderungen über das Sicherheitskonfigurations-Snap-in abruft.</span><span class="sxs-lookup"><span data-stu-id="f7436-105">This is necessary because the attachment snap-in extension gets its data, as well as any changes made by the user, from the Security Configuration snap-in.</span></span> <span data-ttu-id="f7436-106">Dies kann wie im folgenden Verfahren beschrieben erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f7436-106">This can be done as described in the following procedure.</span></span>

<span data-ttu-id="f7436-107">**So richten Sie die Kommunikation mit den Snap-Ins für die Sicherheitskonfiguration ein**</span><span class="sxs-lookup"><span data-stu-id="f7436-107">**To establish communication with the Security Configuration snap-ins**</span></span>

1.  <span data-ttu-id="f7436-108">Rufen Sie den Konfigurations Dateinamen mit dem CCF \_ scesvc- \_ Zwischenablage Format ab, das den Konfigurations Dateinamen als **pwstr** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f7436-108">Obtain the configuration file name using the CCF\_SCESVC\_ATTACHMENT clipboard format, which returns the configuration file name as a **PWSTR**.</span></span>

    <span data-ttu-id="f7436-109">Wenn die Anlage unter einem Knotentyp Knoten eingefügt wird, muss die anlagewissen, welche Konfiguration Sie ist.</span><span class="sxs-lookup"><span data-stu-id="f7436-109">If the attachment is inserted under a configuration type node, the attachment needs to know which configuration it is.</span></span> <span data-ttu-id="f7436-110">(Er kommuniziert diese Informationen an die Sicherheitskonfigurations-Snap-Ins während der Schnittstellen Initialisierung.) Verwenden Sie in diesem Fall den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="f7436-110">(It communicates this information to the Security Configuration snap-ins during interface initialization.) In this case, use the following code.</span></span>

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  <span data-ttu-id="f7436-111">Richten Sie den Kontext mit den Snap-Ins für die Sicherheitskonfiguration ein. Nachdem der Konfigurations Name bekannt ist oder der Dienst Knoten ein Analyse Knoten ist, muss die Erweiterungs-Snap-in-Erweiterung [**iscesvasetachmentdata:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) anrufen, um den Kontext einzurichten, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7436-111">Set up the context with the Security Configuration snap-ins. After the configuration name is known, or if the service node is an analysis node, the attachment snap-in extension must call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to set up the context, as shown in the following example.</span></span>

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
> <span data-ttu-id="f7436-112">Wenn Sie das von [**iscesvcalltachmentdata:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize)zurückgegebene Handle nicht mehr verwenden, schließen Sie das Handle, indem Sie die [**iscesvcalltachmentdata:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f7436-112">When you have finished using the handle returned by [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), close the handle by calling the [**ISceSvcAttachmentData::CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) function.</span></span> <span data-ttu-id="f7436-113">Dies erfolgt in der Regel, wenn der Benutzer die MMC-Konsole schließt.</span><span class="sxs-lookup"><span data-stu-id="f7436-113">This is typically done when the user closes the MMC console.</span></span>

 

 

 



