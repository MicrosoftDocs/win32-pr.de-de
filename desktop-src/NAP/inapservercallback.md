---
title: INapServerCallback-Schnittstelle (NapSystemHealthValidator.h)
description: SHVs verwenden , um den asynchronen Anforderungsabschluss zu signalisieren.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- INapServerCallback-Schnittstelle NAP
- INapServerCallback-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47876290a58d6029559ef4d18baa9067913fe9034cbf218e40f0e382902270e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626150"
---
# <a name="inapservercallback-interface"></a>INapServerCallback-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

**INapServerCallback stellt** eine Methode zur Verfügung, die SHVs verwenden, um den asynchronen Anforderungsabschluss zu signalisieren.

## <a name="members"></a>Member

Die **INapServerCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerCallback** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapServerCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                         | Beschreibung                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback::OnComplete**](inapservercallback-oncomplete-method.md) | Wird von SHVs verwendet, um den asynchronen Anforderungsabschluss zu signalisieren.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

