---
description: Die CIMType-Eigenschaft des SWbemProperty-Objekts ist eine ganze Zahl, mit der der CIM-Typ dieser Eigenschaft bestimmt werden kann. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: SWbemProperty.CIMType-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f3b92cca8d17af8814a7891d0d4f97c7e003b1a999a42c63b6abe59d50e8ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991930"
---
# <a name="swbempropertycimtype-property"></a>SWbemProperty.CIMType-Eigenschaft

Die **CIMType-Eigenschaft** des [**SWbemProperty-Objekts**](swbemproperty.md) ist eine ganze Zahl, mit der der CIM-Typ dieser Eigenschaft bestimmt werden kann. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Weitere Informationen zu gültigen Typen für diese Eigenschaft finden Sie unter [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Instanzen von eingebetteten Objekten werden in zusammengesetzten Objekten als Eigenschaften des Typs **CIM \_ OBJECT** gespeichert. Um die Klasse eines eingebetteten Objekts in einer Instanz einer  zusammengesetzten Klasse zu bestimmen, müssen Sie den CIMType-Qualifizierer der **CIM \_ OBJECT-Typeigenschaft** untersuchen.

Die Objektverweise in einer Zuordnungsklasse werden in Eigenschaften des Typs **CIM \_ REFERENCE** gespeichert. Um die tatsächlichen Objektpfade zu bestimmen, müssen Sie den **CIMType-Qualifizierer** der CIM **\_ REFERENCE-Typeigenschaft** untersuchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




