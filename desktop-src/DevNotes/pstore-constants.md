---
description: Die folgenden Konstanten werden von pstore verwendet.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Pstore-Konstanten (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361497"
---
# <a name="pstore-constants"></a>Pstore-Konstanten

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Die folgenden Konstanten werden von pstore verwendet.

Fehler Codes bei geschützter Speicherung



| Konstante/Wert                                                                                                                                                                                                                               | BESCHREIBUNG                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**PST \_ E \_ OK**</dt> <dt>0x00000000L</dt> </dl>                             | Der Vorgang wurde durchgeführt.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**PST \_ E- \_ Typ ist \_ vorhanden**</dt> <dt>0x800c0004l</dt> </dl> | Das Datenelement ist bereits im geschützten Speicher vorhanden. <br/> |



Access-Klauselwerte



| Konstante/Wert                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**PST \_ Authenticode**</dt> <dt>1</dt> </dl>                       | Verweist auf eine [**PST- \_ authenticodedata**](pst-authenticodedata.md) -Struktur.<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **PST- \_ Binär \_ Überprüfung**</dt> <dt>2</dt> </dl>                   | Verweist auf eine **PST \_ binarycheckdata** -Struktur.<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**PST \_ Sicherheits \_ Beschreibung**</dt> <dt>4</dt> </dl> | Verweist auf eine gültige Windows-Sicherheits Beschreibung. <br/>                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
