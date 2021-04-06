---
title: Ifilllockbytes-Implementierung
description: Das System stellt eine ifilllockbytes-Implementierung als Teil der Implementierung der Verbund Dateien bereit.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- Ifilllockbytes-"STG", Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947685"
---
# <a name="ifilllockbytes---implementation"></a>Ifilllockbytes-Implementierung

Das System stellt eine [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Implementierung als Teil der Implementierung der Verbund Dateien bereit.

Beim Herunterladen von Code kann eine Instanz eines asynchronen Verbund Datei Objekts durch Aufrufen von [**stgopenasyncdocfileonifilllockbytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)erstellt werden. Durch das Herunterladen von Code kann auch eine Instanz eines asynchronen Byte Array-Wrapper Objekts für ein vorhandenes Datei-oder Bytearray erstellt werden, indem entweder die Funktion " [**stggetifilllockbytesonfile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) " oder die Funktion " [**stggetifilllockbytesonilockbytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) " aufgerufen wird.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Derzeit sind URL-Moniker die einzigen Benutzer der asynchronen com-Speicher Implementierung.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die vier Methoden der [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Implementierung.

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**Ifilllockbytes:: fillappend**
</dt> <dd>

Schreibt einen neuen Byte Block an das Ende eines Bytearrays. Die Größe des Blocks wird als Parameter für [**fillappend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)angegeben.

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**Ifilllockbytes:: Fillat**
</dt> <dd>

Schreibt einen neuen Datenblock an eine angegebene Position im Bytearray.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**Ifilllockbytes:: setfillsize**
</dt> <dd>

Legt die Größe des Bytearrays fest. Gibt "E Fail" bei \_ Aufrufen von [**ILockBytes:: Read an**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) zurück, die versuchen, auf Daten über die durch die-Methode angegebene Obergrenze hinaus zuzugreifen.

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**Ifilllockbytes:: beenden**
</dt> <dd>

Informiert das Bytearray, dass ein Download entweder erfolgreich oder erfolglos beendet wurde.

</dd> </dl>

 

 




