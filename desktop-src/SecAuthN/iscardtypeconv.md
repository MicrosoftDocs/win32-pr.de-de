---
description: Stellt die Methoden bereit, die zur Unterstützung der Benutzer der anderen Smartcard-COM-Schnittstellen erforderlich sind.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: ISCardTypeConv-Schnittstelle (Hidddat.h)
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
ms.openlocfilehash: 7fbf009eeeb4f104e5bf09ba8e33b6b2b76eb889a0e44e7594172c697b438d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013590"
---
# <a name="iscardtypeconv-interface"></a>ISCardTypeConv-Schnittstelle

\[Die **ISCardTypeConv-Schnittstelle** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ISCardTypeConv-Schnittstelle** stellt die Methoden bereit, die zur Unterstützung der Benutzer der anderen [*Smartcard-COM-Schnittstellen*](../secgloss/s-gly.md) erforderlich sind. Diese Schnittstelle wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und sollte nicht mehr verwendet werden.

## <a name="members"></a>Member

Die **ISCardTypeConv-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardTypeConv** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardTypeConv-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                              | Beschreibung                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Konvertiert ein typisches C/C++-Bytearray in einen universellen Bytepuffer (**IStream-Objekt).**<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Konvertiert ein Bytearray, das einem universellen Bytepuffer **(IStream-Objekt)** zugeordnet ist, in ein typisches C/C++-Bytearray.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Konvertiert ein Bytearray, das in einen universellen Bytepuffer **(IStream-Objekt)** zugeordnet ist, in ein SAFEARRAY-Objekt ohne Vorzeichen (Byte).<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Konvertiert ein Bytearray, das als SAFEARRAY definiert ist, in einen universellen Bytepuffer (**IStream-Objekt).**<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Erstellt ein Bytearray.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Erstellt einen universellen Puffer von Bytes, die einem **IStream** -Objekt ([**IByteBuffer**](ibytebuffer.md)) zugeordnet sind.<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | Erstellt ein Automation SAFEARRAY-Zeichen ohne Vorzeichen (Bytes).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Gibt einen Arbeitsspeicherzeiger auf den von einer **IStream-COM-Schnittstelle** verwalteten CABLOBAL-Speicherblock frei.<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Erhält einen Bytezeiger auf den CABLOBAL-Speicherblock, der von der **IStream-COM-Schnittstelle** verwaltet wird.<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Bestimmt die Größe (Anzahl von  Bytes) einer IStream-COM-Schnittstelle.<br/>                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Ddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv ist als 53B6AA63-3F56-11D0-916B-00AA00C18068 definiert.<br/>       |



 

 
