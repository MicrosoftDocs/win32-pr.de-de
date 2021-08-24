---
title: IDeliveryOptimizationJob AddFileWithRanges-Methode (Deliveryoptimization.h)
description: Fügt einem Downloadauftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- AddFileWithRanges-Methode
- AddFileWithRanges-Methode, IDeliveryOptimizationJob-Schnittstelle
- IDeliveryOptimizationJob-Schnittstelle, AddFileWithRanges-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 197aa7443123c81d1a675d321b91573823a84f15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476127"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>IDeliveryOptimizationJob::AddFileWithRanges-Methode

Fügt einem Downloadauftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fileId* \[ In\]
</dt> <dd>

Auf NULL beendete Zeichenfolge, die ein eindeutiger Bezeichner des veröffentlichten Inhalts ist. Bei nicht veröffentlichten Inhalten kann dies eine beliebige eindeutige Zeichenfolge sein, die der Aufrufer zum Identifizieren von Dateien innerhalb eines Auftrags verwenden kann.

</dd> <dt>

*remoteUrl* \[ In\]
</dt> <dd>

Auf NULL beendete Zeichenfolge, die den Namen der Datei auf dem Server enthält.

</dd> <dt>

*localName* \[ In\]
</dt> <dd>

Auf NULL beendete Zeichenfolge, die den Namen der Datei auf dem Client enthält.

</dd> <dt>

*rangeCount* \[ in, optional\]
</dt> <dd>

Anzahl der Elemente in *Den Bereichen*.

</dd> <dt>

*Bereiche* \[ in, optional\]
</dt> <dd>

Ein Array von einer oder [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) Strukturen, die die herunterzuladenden Bereiche angeben. Geben Sie keine doppelten oder überlappenden Bereiche an.

</dd> <dt>

*fileSize* \[ in, optional\]
</dt> <dd>

Die Länge der Datei in Bytes. Übergeben Sie **DO_UNKNOWN_FILE_SIZE,** wenn die Größe der Aufruferanwendung nicht bekannt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden Rückgabewerte sowie andere zurück.




| Rückgabecode | Beschreibung | 
|-------------|-------------|
| <dl><dt><strong><strong>S_OK</strong></strong></dt></dl> | Erfolg.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Der lokale Dateiname ist NULL oder eine leere Zeichenfolge. <br /> | 
| <dl><dt><strong>E_ACCESSDENIED</strong></dt></dl> | Der Benutzer verfügt nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis auf dem Client.<br /> | 
| <dl><dt><strong>DO_E_INVALID_RANGE</strong></dt></dl> | Einer der Bereiche ist ungültig. InitialOffset ist z. B. <strong>auf</strong>BG_LENGTH_TO_EOF.<br /> | 
| <dl><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt></dl> | Duplizierte oder überlappende Bereiche können nicht angegeben werden. <br /><blockquote>[!Note]<br />Die Bereiche werden nach dem Offset des Werts und nicht nach der Länge sortiert. Wenn Bereiche eingegeben werden, die den gleichen Offset haben, sich aber in umgekehrter Reihenfolge befinden, wird dieser Fehler zurückgegeben. Wenn beispielsweise 100.5 und 100.0 in dieser Reihenfolge eingegeben werden, können Sie die Datei dem Auftrag nicht hinzufügen.</blockquote><br /> | 
| <dl><dt><strong>DO_E_INVALID_STATE</strong></dt></dl> | Der Status des Auftrags kann nicht <strong>BG_JOB_STATE_CANCELLED</strong> <strong>oder</strong>BG_JOB_STATE_ACKNOWLEDGED.<br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962B3EF7 definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

