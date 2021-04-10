---
title: ResourceLocator. AddOption-Methode (WSManDisp. h)
description: Fügt zusätzliche Daten hinzu, die für die Verarbeitung der Anforderung erforderlich sind. Einige WMI-Anbieter benötigen beispielsweise ein IWbemContext-oder ein Swap-Objekt mit anbieterspezifischen Informationen.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- AddOption-Methode Windows-Remoteverwaltung
- AddOption-Methode Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, AddOption-Methode
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
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040257"
---
# <a name="resourcelocatoraddoption-method"></a>ResourceLocator. AddOption-Methode

Fügt zusätzliche Daten hinzu, die für die Verarbeitung der Anforderung erforderlich sind. Einige WMI-Anbieter benötigen beispielsweise ein [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) -oder ein [**Swap**](/windows/desktop/WmiSdk/swbemnamedvalueset) -Objekt mit anbieterspezifischen Informationen. Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.

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

*OptionName* \[ in\]
</dt> <dd>

Der Name (Schlüssel) des optionalen Datenobjekts.

</dd> <dt>

*OptionValue* \[ in\]
</dt> <dd>

Ein Wert, der für das optionale Datenobjekt angegeben wird.

</dd> <dt>

*mustcompliance* \[ in\]
</dt> <dd>

Ein Flag, das angibt, dass die Option verarbeitet werden muss. Der Standardwert ist **false** (0).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

**Iwsmanresourcelocator:: AddOption** ist die entsprechende C++-Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

