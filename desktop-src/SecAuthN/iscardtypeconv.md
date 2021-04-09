---
description: Stellt die Methoden bereit, die zur Unterstützung der Benutzer der anderen Smartcard-com-Schnittstellen erforderlich sind.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Iscardtypeconfiguration-Schnittstelle (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865039"
---
# <a name="iscardtypeconv-interface"></a>Iscardtypeconfiguration-Schnittstelle

\[Die **iscardtypeconfiguration** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **iscardtypeconfiguration** -Schnittstelle stellt die Methoden bereit, die zur Unterstützung der Benutzer der anderen [*Smartcard*](../secgloss/s-gly.md) -com-Schnittstellen erforderlich sind. Diese Schnittstelle wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und sollte nicht mehr verwendet werden.

## <a name="members"></a>Member

Die **iscardtypeconfiguration** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardtypekonv** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscardtypeconfiguration** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Convertbytearraytbytebuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Konvertiert ein typisches C/C++-Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).<br/>                                   |
| [**Convertbytebuffertbytearray**](iscardtypeconv-convertbytebuffertobytearray.md) | Konvertiert ein Bytearray, das in einen universellen Puffer von Bytes (**IStream** -Objekt) zugeordnet ist, in ein typisches C/C++-Bytearray.<br/>          |
| [**Convertbytebuffertysafearray**](iscardtypeconv-convertbytebuffertosafearray.md) | Konvertiert ein Bytearray, das in einen universellen Puffer von Bytes (**IStream** -Objekt) zugeordnet ist, in ein SAFEARRAY vom Typ Ganzzahl ohne Vorzeichen char (Byte).<br/> |
| [**Converlanafearrayto ByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Konvertiert ein als SAFEARRAY definiertes Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).<br/>                          |
| [**"Kreatebytearray"**](iscardtypeconv-createbytearray.md)                           | Erstellt ein Bytearray.<br/>                                                                                                   |
| [**"Kreatebytebuffer"**](iscardtypeconv-createbytebuffer.md)                         | Erstellt einen universellen Puffer von Bytes, der einem **IStream** -Objekt ([**ibytebuffer**](ibytebuffer.md)) zugeordnet ist.<br/>                  |
| [**"Anatesafearray"**](iscardtypeconv-createsafearray.md)                           | Erstellt ein Automation SafeArray mit nicht signierten Zeichen (Bytes).<br/>                                                              |
| [**Freeistreammemoryptr**](iscardtypeconv-freeistreammemoryptr.md)                 | Gibt einen Speicher Zeiger auf den von einer **IStream** -com-Schnittstelle verwalteten HGLOBAL-Speicherblock frei.<br/>                                  |
| [**Getatistreammemory**](iscardtypeconv-getatistreammemory.md)                     | Ruft einen Byte Zeiger auf den hglobal-Speicherblock ab, der von der **IStream** -com-Schnittstelle verwaltet wird.<br/>                        |
| [**Sizeofstream**](iscardtypeconv-sizeofistream.md)                               | Bestimmt die Größe (Byte Anzahl) einer **IStream** -com-Schnittstelle.<br/>                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.<br/>       |



 

 
