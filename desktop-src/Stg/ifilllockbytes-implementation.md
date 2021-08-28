---
title: 'IFillLockBytes : Implementierung'
description: Das System stellt eine IFillLockBytes-Implementierung als Teil der Compound Files-Implementierung zur Anwendung.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd Stg , Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c095d32bf9a932062b527cd486ee518e099d8de0f0d859caf2f1143e68237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663020"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes : Implementierung

Das System stellt eine [**IFillLockBytes-Implementierung**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) als Teil der Compound Files-Implementierung zur Anwendung.

Durch herunterladen von Code kann eine Instanz eines asynchronen Verbunddateiobjekts erstellt werden, indem [**StgOpenAsyncDocFileOnIFillLockBytes aufgerufen wird.**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes) Das Herunterladen von Code kann auch eine Instanz eines asynchronen Bytearray-Wrapperobjekts für eine vorhandene Datei oder ein Bytearray erstellen, indem entweder die [**StgGetIFillLockBytesOnFile-Funktion**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) oder die [**StgGetIFillLockBytesOnILockBytes-Funktion**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) aufgerufen wird.

## <a name="when-to-use"></a>Verwendung

Derzeit sind URL-Moniker die einzigen Benutzer der asynchronen COM-Speicherimplementierung.

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die vier Methoden der [**IFillLockBytes-Implementierung.**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

Schreibt einen neuen Byteblock an das Ende eines Bytearrays. Die Größe des Blocks wird als Parameter für [**FillAppend angegeben.**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

Schreibt einen neuen Datenblock an eine angegebene Position im Bytearray.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**
</dt> <dd>

Legt die Größe des Bytearrays fest. Gibt E \_ FAIL von Aufrufen von [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) zurück, die versuchen, über die von der -Methode angegebene Obergrenze hinaus auf Daten zu zugreifen.

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**
</dt> <dd>

Informiert das Bytearray darüber, dass ein Download entweder erfolgreich oder nicht erfolgreich beendet wurde.

</dd> </dl>

 

 




