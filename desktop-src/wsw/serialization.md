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
# <a name="serialization"></a><span data-ttu-id="7e0fd-107">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="7e0fd-107">Serialization</span></span>

<span data-ttu-id="7e0fd-108">Serialisierung ist der Prozess zum Schreiben von Werten in C-Datenstrukturen (Strukturen, Arrays und primitive Werte) als XML-Element.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="7e0fd-109">Die Deserialisierung ist der umgekehrte Prozess.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="7e0fd-110">Serialisierung ist der Prozess zum Schreiben von Werten in C-Datenstrukturen (Strukturen, Arrays und primitive Werte) als XML-Element.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="7e0fd-111">Die Deserialisierung ist der umgekehrte Prozess.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="7e0fd-112">Beide Prozesse basieren auf einer Beschreibung der Zuordnung zwischen den C-Datenstrukturen und dem XML-Code.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![Diagramm, das zeigt, wie sich die Serialisierung und Deserialisierung auf eine Beschreibung der Zuordnung zwischen den C-Datenstrukturen und dem XML-Code stützen.](images/xmlmapping.png)

<span data-ttu-id="7e0fd-114">Um einen Wert zu serialisieren, ruft die Anwendung [**wsschreiteelement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**wsschreiteattribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) oder [**wsschreitetype**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)auf.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="7e0fd-115">Um einen Wert zu deserialisieren, ruft die Anwendung [**wsleserelement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**wsread Attribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) oder [**wslestype**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)auf.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="7e0fd-116">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7e0fd-116">Security</span></span>

<span data-ttu-id="7e0fd-117">Der [XML-Reader](xml-reader.md) wird bei der Deserialisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="7e0fd-118">Weitere Informationen zu Sicherheitsinformationen finden Sie im Abschnitt "Sicherheit" in XML Reader.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="7e0fd-119">Das Deserialisierungsprogramm deserialisiert weiterhin Daten, bis das Lesen des deserialisierten Elements abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="7e0fd-120">Der Deserialisierungsprozess schlägt fehl, wenn ein XML-Dokument vorhanden ist, das nicht der Beschreibung der deserialisierten Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="7e0fd-121">An diesem Punkt wird der verwendete XML-Reader ungültig, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="7e0fd-122">Standardmäßig ist die Deserialisierung strikt.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-122">By default deserialization is strict.</span></span> <span data-ttu-id="7e0fd-123">Zu den Bedingungen, bei denen die Deserialisierung fehlschlägt, gehören u. a. folgende:</span><span class="sxs-lookup"><span data-stu-id="7e0fd-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="7e0fd-124">Erwartete Elemente fehlen</span><span class="sxs-lookup"><span data-stu-id="7e0fd-124">Expected elements is missing</span></span>
-   <span data-ttu-id="7e0fd-125">Zwischen den erforderlichen Elementen werden unerwartete Element Felder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="7e0fd-126">Zusätzlicher Element Inhalt nach den erforderlichen Feldern, es sei denn, der **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="7e0fd-127">Unerwartete Attribute, es sei denn, die WS-Struktur ignoriert das Flag für [**\_ \_ \_ nicht behandelte \_ Attribute**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7e0fd-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="7e0fd-128">Unerwarteter Datentyp Wert, der außerhalb des angegebenen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="7e0fd-129">Die Anzahl der sich wiederholenden Elemente liegt außerhalb des angegebenen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="7e0fd-130">Das Serialisieren einer großen Datenmenge kann zu einer übermäßigen Speicher Belegung führen und einen Denial-of-Service-Angriff verursachen.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="7e0fd-131">Der Benutzer, der Daten deserialisiert, muss ein Heap Objekt angeben, um die Daten zuzuordnen, und der Benutzer kann das Heap Zuweisungs Limit verwenden, um Speicher Belegungs Angriffe zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="7e0fd-132">Bereichs Unterstützung für Datentypen, z. b. die maximale Länge für Zeichen folgen, die maximale Element Anzahl im Array usw. ermöglicht dem Benutzer, die maximale Größe für verschiedene Datentypen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="7e0fd-133">Der Benutzer kann einen Bereich in der Daten Beschreibung oder im Schema angeben, um die maximale Größe der unterschiedlichen Daten einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="7e0fd-134">Ein Zeichen folgen Wert, der eine eingebettete NULL-Werte enthält, wird in den Wire-Formaten (Text, Binary, MTOM) unterstützt</span><span class="sxs-lookup"><span data-stu-id="7e0fd-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="7e0fd-135">Wenn eine Zeichenfolge mit einer eingebetteten NULL deserialisiert wird, muss der Benutzer eine gezählte Zeichenfolge (WS-Zeichenfolge) verwenden, \_ damit die NULL-Berechnung nicht mit der Zeichenfolge der Zeichenfolge verwechselt wird.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="7e0fd-136">Wenn ein Zeichen folgen Wert mit einer eingebetteten NULL in ein Feld deserialisiert wird, das eine NULL terminierte Zeichenfolge erwartet, wird ein Fehler zurückgegeben, und die Deserialisierung schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="7e0fd-137">Wenn wsutil zum Generieren von Daten Beschreibungen verwendet wird, sollte die Option/String: WS \_ String verwendet werden, wenn eine Zeichenfolge mit eingebetteter NULL erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="7e0fd-138">Die folgenden Rückrufe werden bei der Serialisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e0fd-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="7e0fd-139">**WS \_ Duration- \_ Vergleichs \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="7e0fd-140">**WS \_ - \_ Lesetyp \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="7e0fd-141">**WS \_ - \_ Schreib \_ typrückruf**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="7e0fd-142">Die folgenden Enumerationen werden bei der Serialisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e0fd-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="7e0fd-143">**WS- \_ Feld \_ Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="7e0fd-144">**WS- \_ Feld \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="7e0fd-145">**WS- \_ Lese \_ Option**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="7e0fd-146">**WS- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="7e0fd-147">**WS \_ - \_ Typzuordnung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="7e0fd-148">**WS- \_ Schreib \_ Option**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="7e0fd-149">Die folgenden Funktionen werden bei der Serialisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e0fd-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="7e0fd-150">**Wslesattribute**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="7e0fd-151">**Wsread Element**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="7e0fd-152">**Wslestype**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="7e0fd-153">**Wsschreiteattribute**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="7e0fd-154">**Wsschreiteelement**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="7e0fd-155">**Wsschreitetype**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="7e0fd-156">Die folgenden Strukturen werden bei der Serialisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e0fd-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="7e0fd-157">**WS- \_ Attribut \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="7e0fd-158">**WS \_ bool- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="7e0fd-159">**Beschreibung der WS- \_ Bytes \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="7e0fd-160">**Beschreibung des WS- \_ Byte- \_ Arrays \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="7e0fd-161">**Beschreibung des WS \_ Char- \_ Arrays \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="7e0fd-162">**\_benutzerdefinierte WS- \_ \_ Typbeschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="7e0fd-163">**WS \_ DateTime- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="7e0fd-164">**WS- \_ Dezimal \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="7e0fd-165">**WS- \_ Standard \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="7e0fd-166">**doppelte WS- \_ \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="7e0fd-167">**Beschreibung der WS- \_ Dauer \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="7e0fd-168">**WS- \_ Element \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="7e0fd-169">**Beschreibung der WS- \_ Endpunkt \_ Adresse \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="7e0fd-170">**WS- \_ Enum- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="7e0fd-171">**WS- \_ \_ Enumerationswert**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="7e0fd-172">**WS- \_ Fehler \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="7e0fd-173">**WS- \_ Feld \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="7e0fd-174">**WS- \_ float- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="7e0fd-175">**WS- \_ GUID- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="7e0fd-176">**WS \_ INT16 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="7e0fd-177">**WS \_ Int32 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="7e0fd-178">**WS \_ Int64 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="7e0fd-179">**WS \_ int8 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="7e0fd-180">**WS- \_ Element \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="7e0fd-181">**WS- \_ Zeichen folgen \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="7e0fd-182">**Beschreibung der WS- \_ Struktur \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="7e0fd-183">**Beschreibung der WS- \_ TimeSpan \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="7e0fd-184">**WS \_ UInt16 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="7e0fd-185">**WS \_ UInt32 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="7e0fd-186">**WS \_ UINT64 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="7e0fd-187">**WS \_ Uint8 \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="7e0fd-188">**Beschreibung der WS- \_ Union \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="7e0fd-189">**Beschreibung der WS- \_ Union- \_ Feld \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="7e0fd-190">**Beschreibung der eindeutigen WS- \_ \_ ID \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="7e0fd-191">**Beschreibung des WS \_ UTF8- \_ Arrays \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="7e0fd-192">**Beschreibung der WS- \_ void \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="7e0fd-193">**WS \_ WSZ- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="7e0fd-194">**WS- \_ XML- \_ QName- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="7e0fd-195">**Beschreibung der WS \_ XML- \_ Zeichenfolge \_**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




