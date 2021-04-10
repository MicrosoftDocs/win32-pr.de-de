---
title: ILockBytes-Implementierung des globalen Speichers
description: Die Implementierung des globalen ILockBytes-Speichers wird in einem Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und für das Lesen und schreiben direkt in den globalen Speicher konzipiert ist.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes, geg, Implementierungen, globaler Speicher
- "\"ILockBytes\", \"STG\", Implementierungen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309472"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes-Implementierung des globalen Speichers

Die Implementierung des globalen ILockBytes-Speichers wird in einem Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und für das Lesen und schreiben direkt in den globalen Speicher konzipiert ist.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Methoden von [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) werden von den Verbund Datei Implementierungen von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf dem Verbund Dateispeicher Objekt aufgerufen, das durch einen Aufruf von [**stganatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)erstellt wurde.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die Methoden der Implementierung des globalen [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -Speichers.

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Read at**
</dt> <dd>

Liest einen Byteblock aus einem angegebenen Offset am Anfang des Bytearrays.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Write-at**
</dt> <dd>

Schreibt den Block von Bytes aus einem angegebenen Offset am Anfang des Bytearrays.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**
</dt> <dd>

Anders als bei der dateibasierten Implementierung hat das Aufrufen dieser Methode in der Implementierung des globalen Speichers keinerlei Auswirkungen.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**
</dt> <dd>

Legt die Größe des Bytearrays fest.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Diese Implementierung unterstützt keine Sperren, weshalb *dwlockstype* auf 0 (null) festgelegt ist. Der Aufrufer muss sicherstellen, dass Zugriffe gültig und sich gegenseitig ausschließen

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Diese Implementierung unterstützt keine Sperren.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

Die von com bereitgestellte [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) -Implementierung ruft die [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) -Methode auf, um Daten zum Bytearray-Objekt abzurufen. Wenn kein angemessener Name für das Bytearray vorhanden ist, gibt die von com bereitgestellte **ILockBytes:: stat** -Methode **null** im **pwcsName** -Member der [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) -Struktur zurück.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




