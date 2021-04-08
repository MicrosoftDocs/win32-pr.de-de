---
description: Die Eigenschaft "CimType" des Objekts "Swap Property" ist eine Ganzzahl, mit der der CIM-Typ dieser Eigenschaft bestimmt werden kann. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: "' Taubemproperty. CimType '-Eigenschaft (wbemdisp. h)"
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
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959904"
---
# <a name="swbempropertycimtype-property"></a>Taubemproperty. CimType (Eigenschaft)

Die Eigenschaft " **CimType** " des Objekts " [**Swap Property**](swbemproperty.md) " ist eine Ganzzahl, mit der der CIM-Typ dieser Eigenschaft bestimmt werden kann. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu gültigen Typen für diese Eigenschaft finden Sie unter [**wbemcimtypeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Instanzen von eingebetteten Objekten werden in zusammengesetzten Objekten als Eigenschaften vom Typ **CIM- \_ Objekt** gespeichert. Um die Klasse eines eingebetteten Objekts in einer Instanz einer zusammengesetzten Klasse zu ermitteln, müssen Sie den **CimType-Qualifizierer** der Eigenschaft **CIM- \_ Objekttyp** überprüfen.

Die Objekt Verweise in einer Association-Klasse werden in Eigenschaften des Typs **CIM- \_ Verweis** gespeichert. Um die eigentlichen Objekt Pfade zu ermitteln, müssen Sie den **CimType-Qualifizierer** der Eigenschaft **CIM- \_ Verweistyp** überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Eigenschaft<br/>                                                         |
| IID<br/>                      | IID \_ iswbemproperty<br/>                                                          |



 

 




