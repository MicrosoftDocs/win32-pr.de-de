---
title: Previewdisplaystyle-Enumeration
description: Wird von iresultviewer PreviewStyle verwendet, um den derzeit verwendeten Anzeige Stil festzulegen oder zu bestimmen.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Previewdisplaystyle-Enumeration Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364461"
---
# <a name="previewdisplaystyle-enumeration"></a>Previewdisplaystyle-Enumeration

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Wird von [**iresultviewer verwendet::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) , um den derzeit verwendeten Anzeige Stil festzulegen oder zu bestimmen.

## <a name="syntax"></a>Syntax


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**
</dt> <dd>

Gibt die AutoPreview an.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**Rechte Vorschau**
</dt> <dd>

Gibt rightpreview an.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**Bottompreview**
</dt> <dd>

Gibt bottompreview an.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Nopreview**
</dt> <dd>

Gibt nopreview an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Wdsview. idl</dt> </dl> |



 

 





