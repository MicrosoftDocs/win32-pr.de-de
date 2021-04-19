---
title: Headerdisplaystyle-Enumeration
description: Wird von iresultviewer HeaderStyle verwendet, um den aktuellen Header Stil festzulegen oder zurückzugeben.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Headerdisplaystyle-Enumeration Legacy Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372373"
---
# <a name="headerdisplaystyle-enumeration"></a>Headerdisplaystyle-Enumeration

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Wird von [**iresultviewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) verwendet, um den aktuellen Header Stil festzulegen oder zurückzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**Fullheader**
</dt> <dd>

Gibt die Verwendung von vollständigen Headern an oder legt diese fest.

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**Kompakter Ader**
</dt> <dd>

Gibt die Verwendung von kompakten Headern an oder legt diese fest.

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noheader**
</dt> <dd>

Gibt die Verwendung von No-Headern an oder legt diese fest.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Wdsview. idl</dt> </dl> |



 

 





