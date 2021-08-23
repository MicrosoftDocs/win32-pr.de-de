---
title: IBackgroundCopyFile5-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie diese Schnittstelle, um generische Eigenschaften von dateiübertragungen Übermittlungsoptimierung (DO) zu erhalten oder zu festlegen.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 369afa2f242faf1572b16f82aebc4ae18a8d501b5e3b806d74bb580beab3aa26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610360"
---
# <a name="ibackgroundcopyfile5-interface"></a>IBackgroundCopyFile5-Schnittstelle

Verwenden Sie diese Schnittstelle, um generische Eigenschaften von dateiübertragungen Übermittlungsoptimierung (DO) zu erhalten oder zu festlegen.

Um einen **IBackgroundCopyFile5-Schnittstellenzeiger** zu erhalten, rufen Sie die **IBackgroundCopyFile::QueryInterface-Methode** mithilfe von __uuidof(IBackgroundCopyFile5) für den Schnittstellenbezeichner auf.

## <a name="members"></a>Member

Die **IBackgroundCopyFile5-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyFile5** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyFile5-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | Ruft den Wert einer generischen BackgroundCopyFile-Eigenschaft ab.<br/> |
| [**Setproperty**](ibackgroundcopyfile5-setproperty.md) | Legt den Wert einer generischen BackgroundCopyFile-Eigenschaft fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 ist als 85C1657F-DAFC-40E8-8834-DF18EA25717E definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

