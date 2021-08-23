---
title: ResultsDisplayStyle-Enumeration
description: Wird von IResultsViewer ResultsStyle verwendet, um festzulegen oder zu bestimmen, wie Ergebnisse angezeigt werden.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- ResultsDisplayStyle-Enumeration– Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: 97a045765b53f29e978c286a14a1d82b86ffb21b5046dee606029a957ee0434c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726525"
---
# <a name="resultsdisplaystyle-enumeration"></a>ResultsDisplayStyle-Enumeration

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Wird von [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) verwendet, um festzulegen oder zu bestimmen, wie Ergebnisse angezeigt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**
</dt> <dd>

Gibt an, dass Ergebnisse als kleine Symbole angezeigt werden.

</dd> <dt>

<span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**
</dt> <dd>

Gibt an, dass Ergebnisse als große Symbole angezeigt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





