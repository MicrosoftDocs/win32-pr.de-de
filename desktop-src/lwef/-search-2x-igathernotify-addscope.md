---
title: IGatherNotify AddScope-Methode (veraltet)
description: Dieses thema Windows Desktopsuche-Schnittstelle ist veraltet und wird durch die Windows Search ISearchPersistentItemsChangedSink-API im Windows SDK ersetzt. | IGatherNotify AddScope-Methode (veraltet)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- AddScope-Methode (veraltet) – Legacy-Windows-Umgebungsfeatures
- AddScope-Methode (veraltet) Legacy Windows Umgebungsfeatures, IGatherNotify-Schnittstelle
- IGatherNotify interface Legacy Windows Environment Features , AddScope (Deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755591"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>IGatherNotify::AddScope-Methode (veraltet)

\[**AddScope** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]

Dieses thema Windows Desktopsuche-Schnittstelle ist veraltet und wird durch die Windows Search [**ISearchPersistentItemsChangedSink-API**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) im Windows SDK ersetzt.

Fügt die Startseite oder URL hinzu, die Sie überwachen. Dies initiiert eine inkrementelle Durchforstung, wenn Sie eine Verbindung herstellen, und geht dann davon aus, dass alle weiteren URL-Änderungen per Benachrichtigung erfolgen.

## <a name="syntax"></a>Syntax


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrScope* \[ In\]
</dt> <dd>

Typ: **BSTR**

Eine Zeichenfolge, die die Startseite oder URLthat angibt, die Sie überwachen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Durch Aufrufen dieser Methode wird eine inkrementelle Durchforstung gestartet, wenn eine Verbindung mit dem Speicher hergestellt wird. Danach wird davon ausgegangen, dass alle URL-Änderungen nach der ersten Aktualisierung per Benachrichtigung erfolgen.

 

 
