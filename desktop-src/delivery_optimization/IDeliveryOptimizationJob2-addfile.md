---
title: IDeliveryOptimizationJob2 AddFile-Methode
description: Die AddFile-Methode fügt einem vorhandenen DO-Auftrag eine einzelne Datei hinzu.
keywords:
- AddFile-Methode
- AddFile-Methode, IDeliveryOptimizationJob2-Schnittstelle
- IDeliveryOptimizationJob2-Schnittstelle, AddFile-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d27bca855bb9c719b485060fabf1f10b7130bd864569e74f98516ca76b8fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544635"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>IDeliveryOptimizationJob2::AddFileWithRanges-Methode

Die AddFile-Methode fügt einem vorhandenen DO-Auftrag eine einzelne Datei hinzu.

## <a name="syntax"></a>Syntax

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*fileId* \[ In\]
</dt> <dd>

Die Datei-ID-Zeichenfolge, die die herunterzuladende Datei eindeutig identifiziert.

</dd> <dt>

*remoteUrl* \[ In\]
</dt> <dd>

Die Datei-URL, die DO versucht, eine Verbindung herzustellen, um die Datei herunterzuladen.

</dd> <dt>

*rangeCount* \[ In\]
</dt> <dd>

Die Anzahl der Elemente, die in Bereichen *enthalten sind.* Ein Nullwert bedeutet, dass keine Bereiche für die Datei verwendet werden.

</dd> <dt>

*Bereiche* \[ In\]
</dt> <dd>

Die optionale Bereichsliste. Jeder Bereich in der Liste ist eine [**BG_FILE_RANGE**](bg-file-range.md) Struktur.

</dd> <dt>

*riid* \[ In\]
</dt> <dd>

Der Objekttyp, der im -Objekt enthalten ist. Dies muss vom Typ IID_IDeliveryOptimizationFile.

</dd> <dt>

*Objekt* \[ out\]
</dt> <dd>

Das IDeliveryOptimizationFile-Objekt, das die Downloaddatei darstellt. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt S_OK bei Erfolg oder einen der HRESULT-Standardwerte bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)  | Windows 10 Desktop-Apps, Version 1803 \[\]                                  |
| Unterstützte Mindestversion (Server)  | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]                              |
| Header                    | Deliveryoptimization.h                                                          |
| Idl                       | DeliveryOptimization.idl                                                        |
| Bibliothek                   | Dosvc.lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962B3EF7 definiert. |

## <a name="see-also"></a>Weitere Informationen:

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
