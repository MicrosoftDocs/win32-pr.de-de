---
title: ILockBytes – Globale Speicherimplementierung
description: Die implementierung des globalen ILockBytes-Speichers wird in einem Bytearrayobjekt implementiert, das einem COM-Verbunddateispeicherobjekt zugrunde liegt, und ist für das direkte Lesen und Schreiben in den globalen Speicher konzipiert.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd Stg , Implementierungen, globaler Arbeitsspeicher
- ILockBytes Strctd Stg , Implementierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f9786f29433bcc02e0b56f3ea9d45c949593f60962e80a650d80ed625da41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867449"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes – Globale Speicherimplementierung

Die implementierung des globalen ILockBytes-Speichers wird in einem Bytearrayobjekt implementiert, das einem COM-Verbunddateispeicherobjekt zugrunde liegt, und ist für das direkte Lesen und Schreiben in den globalen Speicher konzipiert.

## <a name="when-to-use"></a>Verwendung

Methoden von [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) werden von den Verbunddateiimplementierungen von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) für das Verbunddateispeicherobjekt aufgerufen, das durch einen Aufruf von [**StgCreateDocfile erstellt wurde.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die Methoden der [**globalen ILockBytes-Speicherimplementierung.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**
</dt> <dd>

Liest einen Byteblock aus einem angegebenen Offset am Anfang des Bytearrays.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**
</dt> <dd>

Schreibt den Byteblock aus einem angegebenen Offset am Anfang des Bytearrays.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**
</dt> <dd>

Im Gegensatz zur dateibasierten Implementierung hat das Aufrufen dieser Methode in der globalen Speicherimplementierung keine Auswirkungen.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**
</dt> <dd>

Legt die Größe des Bytearrays fest.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**
</dt> <dd>

Diese Implementierung unterstützt keine Sperren, sodass *dwLocksType* auf 0 (null) festgelegt ist. Der Aufrufer muss sicherstellen, dass die Zugriffe gültig sind und sich gegenseitig ausschließen.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**
</dt> <dd>

Diese Implementierung unterstützt keine Sperren.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**
</dt> <dd>

Die von COM bereitgestellte [**IStorage::Stat-Implementierung**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) ruft die [**ILockBytes::Stat-Methode**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) auf, um Daten über das Bytearrayobjekt abzurufen. Wenn kein angemessener Name für das Bytearray vorhanden ist, gibt die von COM bereitgestellte **ILockBytes::Stat-Methode** **NULL** im **pwcsName-Member** der [**STATSTG-Struktur**](/windows/win32/api/objidl/ns-objidl-statstg) zurück.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ilockbytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




