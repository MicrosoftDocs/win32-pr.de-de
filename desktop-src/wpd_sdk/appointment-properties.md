---
description: Tragbare Windows-Geräte unterstützen die folgenden Termin Eigenschaften.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Termin Eigenschaften (portabledevice. h)
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
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362072"
---
# <a name="appointment-properties"></a>Termin Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Termin Eigenschaften.



| Eigenschaft                                   | VarType        | BESCHREIBUNG                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **der WPD- \_ Termin \_ akzeptierte \_ Teilnehmer**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste von Teilnehmern, die den Termin akzeptiert haben.             |
| **WPD- \_ Termin hat \_ \_ Teilnehmer abgelehnt**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste von Teilnehmern, die den Termin abgelehnt haben.             |
| **WPD- \_ Termin \_ Speicherort**             | VT \_ LPWSTR     | Ein leserfreundlicher Ort des Termins, z. b. "Gebäude 5, Raum 7".    |
| **\_ \_ optionale \_ Teilnehmer für WPD-Termin**  | **VT \_ LPWSTR** | Eine durch Semikolons getrennte Liste der optionalen Teilnehmer für den Termin.                  |
| **für WPD- \_ Termin \_ erforderliche \_ Teilnehmer**  | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste der erforderlichen Teilnehmer für den Termin.                  |
| **WPD- \_ Termin \_ Ressourcen**            | **VT \_ LPWSTR** | Durch Semikolons getrennte Liste der für den Termin erforderlichen Ressourcen.                  |
| **\_ \_ vorläufige \_ Teilnehmer für WPD-Termin** | **VT \_ LPWSTR** | Eine durch Semikolons getrennte Liste von Teilnehmern, die den Termin vorläufig akzeptiert haben. |
| **WPD \_ - \_ ereigtentyp**                 | **VT \_ LPWSTR** | Der Typ des Termins, z. b. "persönlich", "Business" usw.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




