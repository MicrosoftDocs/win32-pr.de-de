---
title: Iresultverb Name-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft gibt einen Zeiger auf den Kontonamen für das Verb zurück, z. b. Drucken, öffnen usw.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Namenseigenschaft Legacy-Windows-Umgebungs Features
- Namenseigenschaft Legacy-Windows-Umgebungs Features, iresultverb-Schnittstelle
- Iresultverb Interface Legacy Windows-Umgebungs Features, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949473"
---
# <a name="iresultverbname-property"></a>Iresultverb:: Name-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Diese Eigenschaft gibt einen Zeiger auf den Kontonamen für das Verb zurück, z. b. Drucken, öffnen usw.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

Name ist ein Zeiger auf den Kontonamen für das Verb.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





