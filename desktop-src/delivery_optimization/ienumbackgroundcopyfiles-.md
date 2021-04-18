---
title: Ienumbackgroundcopyfiles-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ienumbackgroundcopyfiles-Schnittstelle zum Auflisten der Dateien, die in einem Auftrag enthalten sind. Um einen ienumbackgroundcopyfiles-Schnittstellen Zeiger abzurufen, nennen Sie die ibackgroundcopyjob-EnumFiles-Methode.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, beschrieben
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
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340330"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Ienumbackgroundcopyfiles-Schnittstelle

Verwenden Sie die **ienumbackgroundcopyfiles** -Schnittstelle zum Auflisten der Dateien, die in einem Auftrag enthalten sind. Um einen **ienumbackgroundcopyfiles** -Schnittstellen Zeiger abzurufen, nennen Sie die [**ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md) -Methode.

## <a name="members"></a>Member

Die **ienumbackgroundcopyfiles** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumbackgroundcopyfiles** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienumbackgroundcopyfiles** -Schnittstelle verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Ruft die Anzahl der Elemente in der-Enumeration ab.<br/>                  |
| [**Weiter**](ienumbackgroundcopyfiles-next.md)         | Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab.<br/> |
| [**Zurücksetzen**](ienumbackgroundcopyfiles-reset.md)       | Setzt die Enumerationsfolge auf den Anfang zurück.<br/>                  |
| [**Überspringen**](ienumbackgroundcopyfiles-skip.md)         | Überspringt eine angegebene Anzahl von Elementen in der Enumerationsfolge.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

