---
description: Die Origin-Eigenschaft des "Swap Property"-Objekts Ruft den Namen der WMI-Klasse ab, in der diese Eigenschaft eingeführt wurde. Für Klassen mit tiefen Vererbungs Hierarchien ist es häufig wünschenswert zu wissen, welche Eigenschaften in welchen Klassen deklariert wurden.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Taubemproperty. Origin-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216317"
---
# <a name="swbempropertyorigin-property"></a>Taubemproperty. Origin (Eigenschaft)

Die **Origin** -Eigenschaft des " [**Swap Property**](swbemproperty.md) "-Objekts Ruft den Namen der WMI-Klasse ab, in der diese Eigenschaft eingeführt wurde. Für Klassen mit tiefen Vererbungs Hierarchien ist es häufig wünschenswert zu wissen, welche Eigenschaften in welchen Klassen deklariert wurden.

Wenn die Eigenschaft lokal ist (siehe " [**austauschen**](swbemqualifier-islocal.md)von"), ist dieser Wert identisch mit der besitzenden Klasse. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a>Eigenschaftswert

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



 

 




