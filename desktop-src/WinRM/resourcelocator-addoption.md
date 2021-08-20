---
title: ResourceLocator.AddOption-Methode (WSManDisp.h)
description: Fügt zusätzliche Daten hinzu, die zum Verarbeiten der Anforderung erforderlich sind. Einige WMI-Anbieter erfordern beispielsweise möglicherweise ein IWbemContext- oder SWbemNamedValueSet-Objekt mit anbieterspezifischen Informationen.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- AddOption-Methode Windows Remoteverwaltung
- AddOption-Methode Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung, AddOption-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c03e587c4884e6d9efc3b98bdd7b41b4204a783e153d9e59a400a4e4bc02a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112965"
---
# <a name="resourcelocatoraddoption-method"></a>ResourceLocator.AddOption-Methode

Fügt zusätzliche Daten hinzu, die zum Verarbeiten der Anforderung erforderlich sind. Einige WMI-Anbieter erfordern beispielsweise möglicherweise ein [**IWbemContext-**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) oder [**SWbemNamedValueSet-Objekt**](/windows/desktop/WmiSdk/swbemnamedvalueset) mit anbieterspezifischen Informationen. Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) angeben, anstatt einen Ressourcen-URI in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)anzugeben.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OptionName* \[ In\]
</dt> <dd>

Der Name (Schlüssel) des optionalen Datenobjekts.

</dd> <dt>

*OptionValue* \[ In\]
</dt> <dd>

Ein für das optionale Datenobjekt bereitgestellter Wert.

</dd> <dt>

*mustComply* \[ In\]
</dt> <dd>

Ein Flag, das angibt, dass die Option verarbeitet werden muss. Der Standardwert ist **False** (0).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**IWSManResourceLocator::AddOption** ist die entsprechende C++-Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

