---
description: Windows Portable Geräte unterstützen die folgenden Termineigenschaften.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Termineigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2ba82c12dfffb0367ab61d355d6e256ab5d97bfbeef3e4a588f3a76a5651f9b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843590"
---
# <a name="appointment-properties"></a>Termineigenschaften

Windows Portable Geräte unterstützen die folgenden Termineigenschaften.



| Eigenschaft                                   | VarType        | Beschreibung                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **\_WPD-TERMIN \_ \_ AKZEPTIERTE TEILNEHMER**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste von Teilnehmern, die den Termin angenommen haben.             |
| **\_WPD-TERMIN \_ \_ ABGELEHNTE TEILNEHMER**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste von Teilnehmern, die den Termin abgelehnt haben.             |
| **WPD \_ APPOINTMENT \_ LOCATION**             | VT \_ LPWSTR     | Ein lesefreundlicher Ort des Termins, z. B. "Gebäude 5, Raum 7".    |
| **\_WPD APPOINTMENT \_ OPTIONALE \_ TEILNEHMER**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste optionaler Teilnehmer für den Termin.                  |
| **WPD \_ APPOINTMENT \_ REQUIRED \_ ATTENDEES**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste der erforderlichen Teilnehmer für den Termin.                  |
| **\_WPD-TERMINRESSOURCEN \_**            | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste von Ressourcen, die für den Termin erforderlich sind.                  |
| **\_WPD-TERMIN \_ – VORLÄUFIGE \_ TEILNEHMER** | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste von Teilnehmern, die den Termin vorläufig angenommen haben. |
| **\_WPD-TERMINTYP \_**                 | **VT \_ LPWSTR** | Der Typ des Termins, z.B. "Persönlich", "Geschäft" usw.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




