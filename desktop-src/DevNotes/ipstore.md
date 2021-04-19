---
description: Stellt com-Standardmethoden zum Verwalten geschützter Speicherdaten Elemente bereit.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Ipstore-Schnittstelle (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373604"
---
# <a name="ipstore-interface"></a>Ipstore-Schnittstelle

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

\[Diese Schnittstelle kann geändert werden oder ist in zukünftigen Versionen von Windows nicht verfügbar.\]

Stellt com-Standardmethoden zum Verwalten geschützter Speicherdaten Elemente bereit. Die [**pstorecreatanstance**](pstorecreateinstance.md) -Methode gibt einen Zeiger auf diese Schnittstelle zurück.

## <a name="members"></a>Member

Die **ipstore** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipstore** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ipstore** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Closeitem**](ipstore-closeitem.md)                   | Schließt ein angegebenes Datenelement aus dem geschützten Speicher.<br/>                                                       |
| [**"Kreatesubtype"**](ipstore-createsubtype.md)           | Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.<br/>                                                   |
| [**CreateType**](ipstore-createtype.md)                 | Erstellt den angegebenen Typ mit dem angegebenen Namen.<br/>                                                        |
| [**DeleteItem**](ipstore-deleteitem.md)                 | Löscht das angegebene Element aus dem geschützten Speicher.<br/>                                                     |
| [**Delta esubtype**](ipstore-deletesubtype.md)           | Löscht den angegebenen Element Untertyp aus dem geschützten Speicher.<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | Löscht den angegebenen Typ aus dem geschützten Speicher.<br/>                                                     |
| [**-Elemente**](ipstore-enumitems.md)                   | Gibt den Schnittstellen Zeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicher Datenbank zurück.<br/>        |
| [**Enumunter Typen**](ipstore-enumsubtypes.md)             | Gibt eine-Schnittstelle zum Auflisten von Untertypen der Typen zurück, die derzeit in der geschützten Datenbank registriert sind.<br/> |
| [**Enumtypes**](ipstore-enumtypes.md)                   | Gibt eine-Schnittstelle zum Auflisten der Typen zurück, die derzeit in der geschützten Datenbank registriert sind.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Ruft Informationen zum Speicher Anbieter ab.<br/>                                                          |
| [**Getprovparam**](ipstore-getprovparam.md)             | Nicht implementiert.<br/>                                                                                           |
| [**Getsubtypeingefo**](ipstore-getsubtypeinfo.md)         | Ruft Informationen ab, die einem Untertyp zugeordnet sind.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Ruft Informationen ab, die einem-Typ zugeordnet sind.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Öffnet ein Element für mehrere Zugriffe.<br/>                                                                       |
| [**"Read accessruleset"**](ipstore-readaccessruleset.md)   | Nicht implementiert.<br/>                                                                                           |
| [**"ReadItem"**](ipstore-readitem.md)                     | Liest das angegebene Datenelement aus dem geschützten Speicher.<br/>                                                      |
| [**Setprovparam**](ipstore-setprovparam.md)             | Legt die angegebenen Parameterinformationen fest.<br/>                                                                  |
| [**"Write-accessruleset"**](ipstore-writeaccessruleset.md) | Nicht implementiert.<br/>                                                                                           |
| [**Schreib Element**](ipstore-writeitem.md)                   | Schreibt ein Datenelement in den geschützten Speicher.<br/>                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
