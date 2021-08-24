---
description: Stellt COM-Standardmethoden zum Verwalten geschützter Speicherdatenelemente zur Verfügung.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: IPStore-Schnittstelle (Pstore.h)
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
ms.openlocfilehash: d6404d182a0c46de222b64892caa8b0e853610c980bfb79d286f781277493cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749706"
---
# <a name="ipstore-interface"></a>IPStore-Schnittstelle

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

\[Diese Schnittstelle kann in zukünftigen Versionen von geändert oder nicht verfügbar Windows.\]

Stellt COM-Standardmethoden zum Verwalten geschützter Speicherdatenelemente zur Verfügung. Die [**PStoreCreateInstance-Methode**](pstorecreateinstance.md) gibt einen Zeiger auf diese Schnittstelle zurück.

## <a name="members"></a>Member

Die **IPStore-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPStore** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IPStore-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | Schließt ein angegebenes Datenelement aus dem geschützten Speicher.<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.<br/>                                                   |
| [**Createtype**](ipstore-createtype.md)                 | Erstellt den angegebenen Typ mit dem angegebenen Namen.<br/>                                                        |
| [**Deleteitem**](ipstore-deleteitem.md)                 | Löscht das angegebene Element aus dem geschützten Speicher.<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | Löscht den angegebenen Elementuntertyp aus dem geschützten Speicher.<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | Löscht den angegebenen Typ aus dem geschützten Speicher.<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | Gibt den Schnittstellenzeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicherdatenbank zurück.<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | Gibt eine Schnittstelle zum Aufzählen von Untertypen der Typen zurück, die derzeit in der geschützten Datenbank registriert sind.<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | Gibt eine Schnittstelle zum Aufzählen der Typen zurück, die derzeit in der geschützten Datenbank registriert sind.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Ruft Informationen zum Speicheranbieter ab.<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | Nicht implementiert.<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | Ruft informationen ab, die einem Untertyp zugeordnet sind.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Ruft einem Typ zugeordnete Informationen ab.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Öffnet ein Element für mehrere Zugriffe.<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | Nicht implementiert.<br/>                                                                                           |
| [**Readitem**](ipstore-readitem.md)                     | Liest das angegebene Datenelement aus dem geschützten Speicher.<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | Legt die angegebenen Parameterinformationen fest.<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | Nicht implementiert.<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | Schreibt ein Datenelement in den geschützten Speicher.<br/>                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
