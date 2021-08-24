---
description: Der CIMType-Qualifizierer enthält Text, der den Typ einer Eigenschaft beschreibt.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: CIMType-Qualifizierer
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
ms.openlocfilehash: 86fad829bf1b2391a9bc97d5c6281a67cadae7d03672e8a6eb8093b7ff6152b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131672"
---
# <a name="cimtype-qualifier"></a>CIMType-Qualifizierer

Der  CIMType-Qualifizierer enthält Text, der den Typ einer Eigenschaft beschreibt.

Dieser Text kann der MOF-Typ sein, z. B. "string" und "sint32" oder der CIM-Typ wie "CIM STRING" und \_ "CIM \_ SINT32". Es gibt eine 1:1-Entsprechung zwischen dem CIMType-Qualifizierer und dem Typ der Eigenschaft, die im *pvtType-Parameter* der  [**IWbemClassObject::Get-Methode verwendet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) wird.

Die beiden Ausnahmen sind:

-   [*Verweiseigenschaften*](gloss-r.md)mit dem Typ **CIM \_ REFERENCE**, die den Wert "REF:classname" enthalten. Der Wert classname beschreibt den Klassentyp der Verweiseigenschaft.
-   Eingebettete Objekteigenschaften, die den **CIM \_ OBJECT-Typ** aufweisen.

Beachten Sie jedoch,  dass der CIMType-Qualifizierer zum genaueren Eingeben einer Verweiseigenschaft verwendet werden kann und sollte. Wenn die Eigenschaft beispielsweise immer auf Instanzen der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) verweist, sollte der CIMType-Qualifizierer auf Folgendes festgelegt werden: 


```mof
"ref:Win32_LogicalDisk"
```



Standardmäßig weist der **CIMType-Qualifizierer** einer Verweiseigenschaft den Typ **ref auf.**

Wie bei Verweiseigenschaften  sollte der CIMType-Qualifizierer verwendet werden, um eine eingebettete Objekteigenschaft mit der folgenden Syntax genauer ein tippen:


```mof
"object:EmbedClass"
```



Da WMI mehr Typen zulässt, als durch Standardkonst constants mit dem VT-Präfix ausgedrückt werden können, kann der CIMType-Qualifizierer beim \_ Interpretieren von Typwerten helfen.  Der  CIMType-Qualifizierer wird automatisch hinzugefügt. Weitere Informationen finden Sie unter [MOF-Datentypen.](mof-data-types.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WMI-Standardqualifizierer**](standard-wmi-qualifiers.md)
</dt> <dt>

[WMI-Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Hinzufügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

