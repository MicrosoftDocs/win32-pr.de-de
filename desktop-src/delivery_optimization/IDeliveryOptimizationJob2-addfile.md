---
title: IDeliveryOptimizationJob2 AddFile-Methode
description: Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.
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
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103246"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>IDeliveryOptimizationJob2:: ADDFILEWITHRANGES-Methode

Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.

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

nicht im  \[ in\]
</dt> <dd>

Die Datei-ID-Zeichenfolge, die die herunter zuladende Datei eindeutig identifiziert.

</dd> <dt>

*RemoteURL* \[ in\]
</dt> <dd>

Die Datei-URL, die versucht, eine Verbindung herzustellen, um die Datei herunterzuladen.

</dd> <dt>

*rangecount* \[ in\]
</dt> <dd>

Die Anzahl der in *Bereichen* enthaltenen Elemente. Ein Wert von 0 (null) bedeutet, dass für die Datei keine Bereiche verwendet werden.

</dd> <dt>

*Bereiche* \[ in\]
</dt> <dd>

Die optionale Bereichs Liste. Jeder Bereich in der Liste ist eine [**BG_FILE_RANGE**](bg-file-range.md) Struktur.

</dd> <dt>

*riid* \[ in\]
</dt> <dd>

Der Typ des Objekts, das im-Objekt enthalten ist. Dies muss vom Typ "IID_IDeliveryOptimizationFile" sein.

</dd> <dt>

*Objekt* \[ vorgenommen\]
</dt> <dd>

Das ideliveryoptimizationfile-Objekt, das die Downloaddatei darstellt. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt S_OK bei Erfolg oder einen der standardmäßigen HRESULT-Werte bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)  | Windows 10, Version 1803, \[ nur Desktop-Apps\]                                  |
| Unterstützte Mindestversion (Server)  | Windows Server, Version 1709, \[ nur Desktop-Apps\]                              |
| Header                    | Deliveryoptimization. h                                                          |
| IDL                       | Deliveryoptimization. idl                                                        |
| Bibliothek                   | Dosvc. lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962b3ef7 definiert. |

## <a name="see-also"></a>Siehe auch

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
