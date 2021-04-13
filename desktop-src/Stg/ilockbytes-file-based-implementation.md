---
title: ILockBytes-File-Based-Implementierung
description: Wird für ein Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und zum Lesen und schreiben direkt in eine Datenträger Datei konzipiert ist.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes-"STG", Implementierungen, Datei basiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388056"
---
# <a name="ilockbytes---file-based-implementation"></a>ILockBytes-File-Based-Implementierung

Wird für ein Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und zum Lesen und schreiben direkt in eine Datenträger Datei konzipiert ist.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Methoden von [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) werden von den Verbund Datei Implementierungen von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf dem Verbund Dateispeicher Objekt aufgerufen, das durch einen Aufruf von [**stganatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)erstellt wurde, sodass Sie Sie nicht direkt aufrufen müssen.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die Methoden der [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -File-Based-Implementierung.

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Read at**
</dt> <dd>

Liest einen Byteblock aus einem angegebenen Offset am Anfang des Byte Arrays.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Write-at**
</dt> <dd>

Schreibt einen Block von Bytes von einem angegebenen Offset am Anfang des Bytearrays.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**
</dt> <dd>

Stellt sicher, dass alle internen Puffer, die von der [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -Implementierung verwaltet werden, in den zugrunde liegenden physischen Speicher geschrieben werden.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**
</dt> <dd>

Legt die Größe des Bytearrays fest.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Der *dwlocktypes* -Parameter ist auf Lock \_ onlyonce oder Lock \_ Exclusive festgelegt, wodurch der Zugriff auf gesperrte Regionen zugelassen oder eingeschränkt wird.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Diese Methode entsperrt den von [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion)gesperrten Bereich.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

Die von com bereitgestellte [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) -Implementierung ruft die [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) -Methode auf, um Informationen zum Bytearray-Objekt abzurufen. Wenn kein angemessener Name für das Bytearray vorhanden ist, gibt die von com bereitgestellte **ILockBytes:: stat** -Methode **null** im **pwcsName** -Member der [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) -Struktur zurück.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




