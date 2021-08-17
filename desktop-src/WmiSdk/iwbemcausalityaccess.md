---
description: Verfolgt untergeordnete Anforderungen nach, die aus einer übergeordneten Anforderung generiert werden.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: IWbemCausalityAccess-Schnittstelle (Wbemint.h)
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
ms.openlocfilehash: a8c71d5b5f59a3b59fe3b639104bfa1fa2dcf9cd35764e37984759827ff7e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131392"
---
# <a name="iwbemcausalityaccess-interface"></a>IWbemCausalityAccess-Schnittstelle

Die **IWbemCausalityAccess-Schnittstelle** verfolgt untergeordnete Anforderungen nach, die aus einer übergeordneten Anforderung generiert werden. Sie können ein **IWbemCausalityAccess-Objekt** mithilfe einer Abfrageschnittstelle (QUERY Interface, QI) für [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)abrufen. Jede Anforderung wird durch eine GUID (Globally Unique Identifier) identifiziert und kann über eine übergeordnete Anforderung verfügen oder eine oberste Anforderung sein. Eine GUID ist eine eindeutige 128-Bit-Zahl. Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.

## <a name="members"></a>Member

Die **IWbemCausalityAccess-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWbemCausalityAccess** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWbemCausalityAccess-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | Beschreibung                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestId**](iwbemcausalityaccess-getrequestid.md) | Gibt einen eindeutigen GUID-Bezeichner für eine Anforderung zurück.<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | Bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen übergeordneten Anforderung ist. Eine übergeordnete Anforderung kann mehrere untergeordnete Anforderungen aufweisen, die jeweils durch einen eindeutigen GUID-Wert identifiziert werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM-API für WMI](com-api-for-wmi.md)
</dt> </dl>

 

