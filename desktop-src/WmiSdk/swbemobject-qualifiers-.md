---
description: Die \_ Qualifiers-Eigenschaft des SWbemObject-Objekts gibt ein SWbemQualifierSet-Objekt zurück, das eine Auflistung der Qualifizierer für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3096b11399336a7dfcd9a36a314f6e569e24b29e8d27718345adbb55a9af0107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732490"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject.Qualifiers-Eigenschaft \_

Die **\_ Qualifiers-Eigenschaft** des [**SWbemObject-Objekts**](swbemobject.md) gibt ein [**SWbemQualifierSet-Objekt**](swbemqualifierset.md) zurück, das eine Auflistung der Qualifizierer für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Das VbScript-Codebeispiel [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) im TechNet Gallery verwendet die Qualifier-Eigenschaft, um die \_ Klassenqualifizierer für eine angegebene WMI-Klasse aufzulisten.

Im Codebeispiel List All Abstract Classes in WMI VBScript [(Alle abstrakten Klassen in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript auflisten) im TechNet-Katalog werden alle abstrakten WMI-Klassen aufgelistet, die im \\ cimv2-Stammnamespace definiert sind.

Im Codebeispiel List All Dynamic Classes in WMI VBScript [(Alle dynamischen Klassen in WMI-VBScript](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) auflisten) wird die Qualifier-Eigenschaft \_ verwendet, um alle dynamischen WMI-Klassen (einschließlich Zuordnungsklassen) aufzulisten, die im \\ cimv2-Stammnamespace definiert sind.

Im [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell-Codebeispiel im TechNet-Katalog werden alle beschreibbaren Eigenschaften im angegebenen Namespace aufgelistet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




