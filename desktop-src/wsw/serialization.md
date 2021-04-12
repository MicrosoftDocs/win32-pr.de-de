---
title: Serialisierung
description: Serialisierung ist der Prozess zum Schreiben von Werten in C-Datenstrukturen (Strukturen, Arrays und primitive Werte) als XML-Element. Die Deserialisierung ist der umgekehrte Prozess.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Serialisierungsweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104218950"
---
# <a name="serialization"></a>Serialisierung

Serialisierung ist der Prozess zum Schreiben von Werten in C-Datenstrukturen (Strukturen, Arrays und primitive Werte) als XML-Element. Die Deserialisierung ist der umgekehrte Prozess.


Serialisierung ist der Prozess zum Schreiben von Werten in C-Datenstrukturen (Strukturen, Arrays und primitive Werte) als XML-Element. Die Deserialisierung ist der umgekehrte Prozess.

Beide Prozesse basieren auf einer Beschreibung der Zuordnung zwischen den C-Datenstrukturen und dem XML-Code.

![Diagramm, das zeigt, wie sich die Serialisierung und Deserialisierung auf eine Beschreibung der Zuordnung zwischen den C-Datenstrukturen und dem XML-Code stützen.](images/xmlmapping.png)

Um einen Wert zu serialisieren, ruft die Anwendung [**wsschreiteelement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**wsschreiteattribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) oder [**wsschreitetype**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)auf.

Um einen Wert zu deserialisieren, ruft die Anwendung [**wsleserelement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**wsread Attribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) oder [**wslestype**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)auf.

## <a name="security"></a>Sicherheit

Der [XML-Reader](xml-reader.md) wird bei der Deserialisierung verwendet. Weitere Informationen zu Sicherheitsinformationen finden Sie im Abschnitt "Sicherheit" in XML Reader.

Das Deserialisierungsprogramm deserialisiert weiterhin Daten, bis das Lesen des deserialisierten Elements abgeschlossen ist. Der Deserialisierungsprozess schlägt fehl, wenn ein XML-Dokument vorhanden ist, das nicht der Beschreibung der deserialisierten Daten entspricht. An diesem Punkt wird der verwendete XML-Reader ungültig, und es wird ein Fehler zurückgegeben.

Standardmäßig ist die Deserialisierung strikt. Zu den Bedingungen, bei denen die Deserialisierung fehlschlägt, gehören u. a. folgende:

-   Erwartete Elemente fehlen
-   Zwischen den erforderlichen Elementen werden unerwartete Element Felder angezeigt.
-   Zusätzlicher Element Inhalt nach den erforderlichen Feldern, es sei denn, der **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Unerwartete Attribute, es sei denn, die WS-Struktur ignoriert das Flag für [**\_ \_ \_ nicht behandelte \_ Attribute**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) .
-   Unerwarteter Datentyp Wert, der außerhalb des angegebenen Bereichs liegt.
-   Die Anzahl der sich wiederholenden Elemente liegt außerhalb des angegebenen Bereichs.

Das Serialisieren einer großen Datenmenge kann zu einer übermäßigen Speicher Belegung führen und einen Denial-of-Service-Angriff verursachen. Der Benutzer, der Daten deserialisiert, muss ein Heap Objekt angeben, um die Daten zuzuordnen, und der Benutzer kann das Heap Zuweisungs Limit verwenden, um Speicher Belegungs Angriffe zu verhindern.

Bereichs Unterstützung für Datentypen, z. b. die maximale Länge für Zeichen folgen, die maximale Element Anzahl im Array usw. ermöglicht dem Benutzer, die maximale Größe für verschiedene Datentypen zu steuern. Der Benutzer kann einen Bereich in der Daten Beschreibung oder im Schema angeben, um die maximale Größe der unterschiedlichen Daten einzuschränken.

Ein Zeichen folgen Wert, der eine eingebettete NULL-Werte enthält, wird in den Wire-Formaten (Text, Binary, MTOM) unterstützt Wenn eine Zeichenfolge mit einer eingebetteten NULL deserialisiert wird, muss der Benutzer eine gezählte Zeichenfolge (WS-Zeichenfolge) verwenden, \_ damit die NULL-Berechnung nicht mit der Zeichenfolge der Zeichenfolge verwechselt wird. Wenn ein Zeichen folgen Wert mit einer eingebetteten NULL in ein Feld deserialisiert wird, das eine NULL terminierte Zeichenfolge erwartet, wird ein Fehler zurückgegeben, und die Deserialisierung schlägt fehl. Wenn wsutil zum Generieren von Daten Beschreibungen verwendet wird, sollte die Option/String: WS \_ String verwendet werden, wenn eine Zeichenfolge mit eingebetteter NULL erwartet wird.

Die folgenden Rückrufe werden bei der Serialisierung verwendet:

-   [**WS \_ Duration- \_ Vergleichs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**WS \_ - \_ Lesetyp \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS \_ - \_ Schreib \_ typrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

Die folgenden Enumerationen werden bei der Serialisierung verwendet:

-   [**WS- \_ Feld \_ Zuordnung**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**WS- \_ Feld \_ Optionen**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**WS- \_ Lese \_ Option**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**WS- \_ Typ**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**WS \_ - \_ Typzuordnung**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**WS- \_ Schreib \_ Option**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

Die folgenden Funktionen werden bei der Serialisierung verwendet:

-   [**Wslesattribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**Wsread Element**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**Wslestype**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**Wsschreiteattribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**Wsschreiteelement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**Wsschreitetype**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

Die folgenden Strukturen werden bei der Serialisierung verwendet:

-   [**WS- \_ Attribut \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**WS \_ bool- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**Beschreibung der WS- \_ Bytes \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**Beschreibung des WS- \_ Byte- \_ Arrays \_**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**Beschreibung des WS \_ Char- \_ Arrays \_**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**\_benutzerdefinierte WS- \_ \_ Typbeschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**WS \_ DateTime- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**WS- \_ Dezimal \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**WS- \_ Standard \_ Wert**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**doppelte WS- \_ \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**Beschreibung der WS- \_ Dauer \_**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**WS- \_ Element \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**Beschreibung der WS- \_ Endpunkt \_ Adresse \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**WS- \_ Enum- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**WS- \_ \_ Enumerationswert**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**WS- \_ Fehler \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**WS- \_ Feld \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**WS- \_ float- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**WS- \_ GUID- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**WS \_ INT16 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**WS \_ Int32 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**WS \_ Int64 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**WS \_ int8 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**WS- \_ Element \_ Bereich**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**WS- \_ Zeichen folgen \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**Beschreibung der WS- \_ Struktur \_**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**Beschreibung der WS- \_ TimeSpan \_**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**WS \_ UInt16 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**WS \_ UInt32 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**WS \_ UINT64 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**WS \_ Uint8 \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**Beschreibung der WS- \_ Union \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**Beschreibung der WS- \_ Union- \_ Feld \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**Beschreibung der eindeutigen WS- \_ \_ ID \_**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**Beschreibung des WS \_ UTF8- \_ Arrays \_**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**Beschreibung der WS- \_ void \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**WS \_ WSZ- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**WS- \_ XML- \_ QName- \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**Beschreibung der WS \_ XML- \_ Zeichenfolge \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




