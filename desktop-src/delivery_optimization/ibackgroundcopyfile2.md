---
title: IBackgroundCopyFile2-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie die IBackgroundCopyFile2-Schnittstelle, um einen neuen Remotenamen für die Datei anzugeben und die Liste der herunterzuladenden Bereiche abzurufen.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f185fef1ddaa9ceb4298f3e8916bb3d207b311b300f0071d601aadf47b0777a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853860"
---
# <a name="ibackgroundcopyfile2-interface"></a>IBackgroundCopyFile2-Schnittstelle

Verwenden Sie **die IBackgroundCopyFile2-Schnittstelle,** um einen neuen Remotenamen für die Datei anzugeben und die Liste der herunterzuladenden Bereiche abzurufen.

Die **IBackgroundCopyFile2-Schnittstelle** erbt von der [**IBackgroundCopyFile-Schnittstelle.**](ibackgroundcopyfile.md)

Um einen **IBackgroundCopyFile2-Schnittstellenzeiger** zu erhalten, rufen Sie die **IBackgroundCopyFile::QueryInterface-Methode** mithilfe von __uuidof(IBackgroundCopyFile2) für den Schnittstellenbezeichner auf. Verwenden Sie **den IBackgroundCopyFile2-Schnittstellenzeiger,** um sowohl die [**IBackgroundCopyFile-**](ibackgroundcopyfile.md) als auch **die IBackgroundCopyFile2-Methode auf** aufruft.

## <a name="members"></a>Member

Die **IBackgroundCopyFile2-Schnittstelle** erbt von [**IBackgroundCopyFile**](ibackgroundcopyfile.md). **IBackgroundCopyFile2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyFile2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                             | Beschreibung                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Ruft das Array von Bereichen ab, die Sie aus der URL herunterladen möchten.<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | Ändert den Remotenamen in eine neue URL.<br/>                                 |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 ist als 83E81B93-0873-474D-8A8C-F2018B1A939C definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





