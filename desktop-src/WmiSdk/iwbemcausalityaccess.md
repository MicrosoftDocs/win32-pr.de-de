---
description: Verfolgt die untergeordneten Anforderungen, die von einer übergeordneten Anforderung generiert werden.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Iwbemkausalityaccess-Schnittstelle (wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359205"
---
# <a name="iwbemcausalityaccess-interface"></a>Iwbemkausalityaccess-Schnittstelle

Die **iwbemkausalityaccess** -Schnittstelle verfolgt die untergeordneten Anforderungen, die von einer übergeordneten Anforderung generiert werden. Sie können ein **iwbemkausalityaccess** -Objekt mit einer Abfrage Schnittstelle (Qi) für [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)abrufen. Jede Anforderung wird durch einen global eindeutigen Bezeichner (GUID) identifiziert und kann über eine übergeordnete Anforderung verfügen oder eine Top-Anforderung sein. Eine GUID ist eine eindeutige 128-Bit-Zahl. Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.

## <a name="members"></a>Member

Die **iwbemkausalityaccess** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwbemkausalityaccess** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwbemkausalityaccess** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestID**](iwbemcausalityaccess-getrequestid.md) | Gibt einen eindeutigen GUID-Bezeichner für eine Anforderung zurück.<br/>                                                                                                              |
| [**Ischildof**](iwbemcausalityaccess-ischildof.md)       | Bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen übergeordneten Anforderung ist. Eine übergeordnete Anforderung kann über mehrere untergeordnete Anforderungen verfügen, die jeweils durch einen eindeutigen GUID-Wert identifiziert werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM-API für WMI](com-api-for-wmi.md)
</dt> </dl>

 

