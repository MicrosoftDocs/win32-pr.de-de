---
description: Der CimType-Qualifizierer enthält Text, der den Typ einer Eigenschaft beschreibt.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: CimType-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131984"
---
# <a name="cimtype-qualifier"></a>CimType-Qualifizierer

Der **CimType-Qualifizierer** enthält Text, der den Typ einer Eigenschaft beschreibt.

Dieser Text kann der MOF-Typ sein, z. b. "String" und "sint32", oder der CIM-Typ, z. b. "CIM \_ String" und "CIM \_ sint32". Zwischen dem **CimType-Qualifizierer** und dem Typ der Eigenschaft, der im *pvttype* -Parameter der [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) -Methode verwendet wird, besteht eine eins-zu-eins-Entsprechung.

Die beiden Ausnahmen lauten:

-   [*Verweis Eigenschaften*](gloss-r.md)mit dem Type- **CIM- \_ Verweis**, der den Wert "Ref: ClassName" enthält. Der ClassName-Wert beschreibt den Klassentyp der Verweis Eigenschaft.
-   Eigenschaften von eingebetteten Objekten, die den **CIM \_ -Objekttyp** aufweisen.

Beachten Sie jedoch, dass der **CimType-Qualifizierer** und verwendet werden kann, um eine Verweis Eigenschaft genauer einzugeben. Wenn sich die-Eigenschaft beispielsweise immer auf Instanzen der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse bezieht, sollte der **CimType-Qualifizierer** auf Folgendes festgelegt werden:


```mof
"ref:Win32_LogicalDisk"
```



Standardmäßig hat der **CimType-Qualifizierer** einer Verweis Eigenschaft den Typ **ref**.

Wie bei den Verweis Eigenschaften sollte der **CimType-Qualifizierer** zum Eingeben einer eingebetteten Objekt Eigenschaft genau mit der folgenden Syntax verwendet werden:


```mof
"object:EmbedClass"
```



Da WMI mehr Typen zulässt, als durch Standard Konstanten mit dem VT-Präfix ausgedrückt werden können \_ , kann der **CimType-Qualifizierer** helfen, Typwerte zu interpretieren. Der **CimType-Qualifizierer** wird automatisch hinzugefügt. Weitere Informationen finden Sie unter [MOF-Datentypen](mof-data-types.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WMI-Standard Qualifizierer**](standard-wmi-qualifiers.md)
</dt> <dt>

[WMI Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Fügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

