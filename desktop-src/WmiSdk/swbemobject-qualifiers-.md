---
description: Die \_ qualifizierereigenschaft des Objekts "errbewbject" gibt ein "errbemqualifierset"-Objekt zurück, das eine Auflistung der Qualifizierer für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_-Eigenschaft (wbemdisp. h)
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
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348882"
---
# <a name="swbemobjectqualifiers_-property"></a>"Errbemubject. \_ qualifizierereigenschaft"

Die **\_ qualifizierereigenschaft** des Objekts " [**errbewbject**](swbemobject.md) " gibt ein " [**errbemqualifierset**](swbemqualifierset.md) "-Objekt zurück, das eine Auflistung der Qualifizierer für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Die [Liste alle Qualifizierer für ein WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) -VBScript-Codebeispiel in der TechNet Gallery verwendet die \_ qualifizierereigenschaft, um die Klassen Qualifizierer für eine angegebene WMI-Klasse aufzulisten.

Im Codebeispiel [List All Abstract classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript in der TechNet Gallery werden alle WMI-abstrakten Klassen aufgelistet, die im root \\ CIMV2-Namespace definiert sind.

Im Codebeispiel [List All Dynamic classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript wird die qualifizierereigenschaft verwendet \_ , um alle dynamischen WMI-Klassen (einschließlich Association-Klassen) aufzulisten, die im Stamm- \\ CIMV2-Namespace definiert sind.

Das [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell-Codebeispiel in der TechNet Gallery listet alle beschreibbaren Eigenschaften im angegebenen Namespace auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



 

 




