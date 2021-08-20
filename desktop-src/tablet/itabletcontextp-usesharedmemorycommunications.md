---
description: Ermöglicht den Zugriff auf Den Arbeitsspeicher, der von Tabletthreads gemeinsam genutzt wird.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: ITabletContextP::UseSharedMemoryCommunications-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: e8ee871cf24c4a853b01d9f4d351caeabbff9edcfe4ce7d8c8221eb0ace0472a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041894"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>ITabletContextP::UseSharedMemoryCommunications-Methode

Ermöglicht den Zugriff auf Den Arbeitsspeicher, der von Tabletthreads gemeinsam genutzt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pid* \[ In\]
</dt> <dd>

Prozess-ID.

</dd> <dt>

*phEventMoreData* \[ out\]
</dt> <dd>

Ereignishand handle, das signalisiert, wenn neue Daten für die Verarbeitung verfügbar sind.

</dd> <dt>

*phEventClientReady* \[ out\]
</dt> <dd>

Gibt ein Ereignishand handle zurück, das verwendet wird, um zu signalisieren, dass der Client zum Empfangen von Daten bereit ist. Signalisiert nach der Verarbeitung neuer Daten.

</dd> <dt>

*phMutexAccess* \[ out\]
</dt> <dd>

Der Mutex, der Zugriff auf freigegebenen Speicher gewährt.

</dd> <dt>

*phFileMapping* \[ out\]
</dt> <dd>

Zeiger auf den Freigegebenen Speicherblock.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **UseSharedMemoryCommunications-Methode** wird als Teil des Freigegebenen Speicherprotokolls des Tablet-PCs verwendet. Da der Wispprivileg-Dienst über eine hohe Integritätsebene (High Integrity Level, IL) verfügt, kann er daten speichern und darauf zugreifen, die im freigegebenen Speicher gespeichert sind, ohne seine Berechtigungen erhöhen zu müssen.

Die [**SHAREDMEMORY \_ HEADER-Struktur**](sharedmemory-header.md) wird aus den Daten, auf die von der Dateizuordnung verwiesen wird, und die Rohdaten des Pakets folgen **dem SHAREDMEMORY-HEADER \_**. Unformatierte Paketdaten können aus dem freigegebenen Speicher gelesen werden, wenn das Ereignis ausgelöst wird, auf das *pdwEventClientReady* verweist.

In der folgenden Liste wird die Abfolge von Ereignissen für den Zugriff auf und die Verwendung von freigegebenen Speicher beschrieben.

-   Der Client legt das clientReady-Ereignis fest.
-   Der Client wartet auf das MoreData-Ereignis.
-   Der Client übernimmt den Mutex.
-   Der Client liest Paketdaten aus dem Abschnitt des freigegebenen Speichers nach dem Header und den Seriennummern nach den Paketen.
-   Der Client verarbeitet Daten abhängig vom Wert von **dwEvent**.
-   Der Client schreibt -1 (0xFFFFFFFF) in **dwEvent**.
-   Der Client gibt den Mutex frei.
-   Der Client legt das clientReady-Ereignis fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITabletContextP-Schnittstelle**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




