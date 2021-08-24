---
title: IEnumBackgroundCopyFiles-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie die IEnumBackgroundCopyFiles-Schnittstelle, um die Dateien aufzählen, die ein Auftrag enthält. Um einen IEnumBackgroundCopyFiles-Schnittstellenzeiger zu erhalten, rufen Sie die IBackgroundCopyJob EnumFiles-Methode auf.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- IEnumBackgroundCopyFiles-Schnittstelle
- IEnumBackgroundCopyFiles-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c6cf97975d583a99145e32482bc097ebd6ce3cc052e62560a34f7f78c1f88ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635680"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>IEnumBackgroundCopyFiles-Schnittstelle

Verwenden Sie **die IEnumBackgroundCopyFiles-Schnittstelle,** um die Dateien aufzählen, die ein Auftrag enthält. Um einen **IEnumBackgroundCopyFiles-Schnittstellenzeiger** zu erhalten, rufen Sie die [**IBackgroundCopyJob::EnumFiles-Methode**](ibackgroundcopyjob-enumfiles.md) auf.

## <a name="members"></a>Member

Die **IEnumBackgroundCopyFiles-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumBackgroundCopyFiles** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumBackgroundCopyFiles-Schnittstelle** verfügt über diese Methoden.



| Methode                                                | Beschreibung                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Ruft die Anzahl der Elemente in der -Enumeration ab.<br/>                  |
| [**Weiter**](ienumbackgroundcopyfiles-next.md)         | Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab.<br/> |
| [**Zurücksetzen**](ienumbackgroundcopyfiles-reset.md)       | Setzt die Enumerationsfolge auf den Anfang zurück.<br/>                  |
| [**Überspringen**](ienumbackgroundcopyfiles-skip.md)         | Überspringt eine angegebene Anzahl von Elementen in der Enumerationsfolge.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

