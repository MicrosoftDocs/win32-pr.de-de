---
title: Imsrdpinputsink-Schnittstelle
description: Eingabe Senke für Remote Desktop.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Imsrdpinputsink-Schnittstelle Remotedesktopdienste
- Imsrdpinputsink-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949626"
---
# <a name="imsrdpinputsink-interface"></a>Imsrdpinputsink-Schnittstelle

Eingabe Senke für Remote Desktop.

## <a name="members"></a>Member

Die **imsrdpinputsink** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imsrdpinputsink** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imsrdpinputsink** -Schnittstelle verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**Addtouchinput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Fügt Berührungs Eingaben hinzu.<br/>         |
| [**Begintouchframe**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Beginn des Berührungs Rahmens.<br/>        |
| [**Endtouchframe**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Ende des Berührungs Rahmens.<br/>          |
| [**Sendkeyboarde Vent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Sendet ein Tastaturereignis.<br/>     |
| [**Sendmouslibuttonevent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Sendet das Maustasten Ereignis.<br/> |
| [**Sendmoussmuveevent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Sendet das MouseMove-Ereignis.<br/>   |
| [**Sendmouserwheelevent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Sendet ein Mausrad Ereignis.<br/>  |
| [**Sendsyncevent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Sendet ein Synchronisierungs Ereignis.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                      |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpinputsink ist definiert als 4606850e-76a7-4e28-a47e-c7174f 619351<br/>     |



 

