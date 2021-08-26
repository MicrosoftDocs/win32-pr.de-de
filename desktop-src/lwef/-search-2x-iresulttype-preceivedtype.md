---
title: IResultType PreceivedType-Eigenschaft (WdsSharedIDL.h)
description: Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- PreceivedType-Eigenschaft Legacy Windows-Umgebungsfeatures
- PreceivedType-Eigenschaft Legacy Windows Umgebungsfeatures, IResultType-Schnittstelle
- IResultType-Schnittstelle Legacy Windows Umgebungsfeatures, PreceivedType-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765a770dc07f1fc0287e861ca79fc2aa941ea7cc425fff29e5e4c5772410c06e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014616"
---
# <a name="iresulttypepreceivedtype-property"></a>IResultType::P receivedType-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt die Adresse der Zeichenfolge zurück, die den Typ im Index identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





