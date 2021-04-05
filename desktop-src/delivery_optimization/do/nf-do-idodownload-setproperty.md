---
title: 'Idodownload:: SetProperty-Methode'
description: Legt eine Download Eigenschaft fest.
keywords:
- 'Idodownload:: SetProperty-Methode'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719565"
---
# <a name="idodownloadsetproperty-method"></a>Idodownload:: SetProperty-Methode

Legt eine Download Eigenschaft fest. Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die eine bestimmte Eigenschaft enthält, die auf den Download angewendet werden soll.

## <a name="syntax"></a>Syntax

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche eigen schafts-ID, die festgelegt werden soll (vom Typ **dodownloadproperty**).

`propVal`

Der festzulegende Eigenschafts Wert, der in einem **Variant** gespeichert wird.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*PROPID* ist unbekannt.|
|DO_E_INVALID_STATE|Der Download befindet sich derzeit nicht in einem Zustand, der das Festlegen von Eigenschaften zulässt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
