---
title: Resultendisplaystyle-Enumeration
description: Wird von iresultviewer resultstyle verwendet, um festzulegen, wie Ergebnisse angezeigt werden, oder legt diese fest.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Resultdisplaystyle-Enumeration Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369216"
---
# <a name="resultsdisplaystyle-enumeration"></a>Resultendisplaystyle-Enumeration

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Wird von [**iresultviewer:: resultstyle**](-search-2x-iresultsviewer-resultsstyle.md) verwendet, um festzulegen oder zu bestimmen, wie Ergebnisse angezeigt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**Smallireresults**
</dt> <dd>

Gibt an, dass die Ergebnisse als kleine Symbole angezeigt werden.

</dd> <dt>

<span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**Largeireresults**
</dt> <dd>

Gibt an, dass die Ergebnisse als große Symbole angezeigt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Wdsview. idl</dt> </dl> |



 

 





