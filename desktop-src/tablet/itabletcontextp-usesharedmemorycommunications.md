---
description: Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Itabletcontextp:: geesharedmemorycommunications-Methode'
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
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353989"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>Itabletcontextp:: geesharedmemorycommunications-Methode

Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben

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

*PID* \[ in\]
</dt> <dd>

Prozess-ID.

</dd> <dt>

*pheventmoredata* \[ vorgenommen\]
</dt> <dd>

Ereignis handle, das signalisiert, wann neue Daten zur Verarbeitung verfügbar sind.

</dd> <dt>

*pheventclientready* \[ vorgenommen\]
</dt> <dd>

Zurück gegebenes Ereignis handle, mit dem signalisiert wird, dass der Client für den Empfang von Daten bereit ist. Wird signalisiert, nachdem neue Daten verarbeitet wurden.

</dd> <dt>

*phmutexaccess* \[ vorgenommen\]
</dt> <dd>

Der Mutex, der Zugriff auf den gemeinsamen Speicher gewährt.

</dd> <dt>

*phfilemapping* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den freigegebenen Speicherblock.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Methode " **toharedmemorycommunications** " wird als Teil des Tablet PC Shared Memory-Protokolls verwendet. Da der wisptis-Dienst über eine hohe Integritäts Ebene (High Integrity Level, IL) verfügt, kann er Daten, die im freigegebenen Speicher gespeichert sind, speichern und darauf zugreifen.

Die [**SharedMemory- \_ Header**](sharedmemory-header.md) Struktur wird aus den Daten, auf die die Datei Zuordnung verweist, umgewandelt, und die unformatierten Paketdaten folgen dem **SharedMemory- \_ Header**. Rohdaten von Paketen können aus dem freigegebenen Speicher gelesen werden, wenn das Ereignis, auf das *pdweventclientready* verweist, ausgelöst wird.

In der folgenden Liste wird die Abfolge von Ereignissen zum Zugreifen auf und Verwenden von frei gegebenem Speicher beschrieben.

-   Der Client legt das clientready-Ereignis fest.
-   Der Client wartet auf das MoreData-Ereignis.
-   Der Client erhält den Mutex.
-   Der Client liest Paketdaten aus dem Abschnitt des gemeinsam genutzten Speichers nach dem Header und den Seriennummern nach den Paketen.
-   Der Client verarbeitet Daten abhängig vom Wert von **dwevent**.
-   Der Client schreibt-1 (0xFFFFFFFF) in **dwevent**.
-   Der Client gibt den Mutex frei.
-   Der Client legt das clientready-Ereignis fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletcontextp-Schnittstelle**](itabletcontextp.md)
</dt> <dt>

[**Usenamedsharedmemorycommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




