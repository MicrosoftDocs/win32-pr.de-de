---
description: Die PropertyInfo-Datenstruktur definiert eine Eigenschaft des Protokolls.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: PropertyInfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959488"
---
# <a name="propertyinfo-structure"></a><span data-ttu-id="c4644-103">PropertyInfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="c4644-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="c4644-104">Die **PropertyInfo** -Datenstruktur definiert eine Eigenschaft des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="c4644-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4644-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4644-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a><span data-ttu-id="c4644-106">Member</span><span class="sxs-lookup"><span data-stu-id="c4644-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4644-107">**hproperty**</span><span class="sxs-lookup"><span data-stu-id="c4644-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-108">Legen Sie dieses Feld auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="c4644-108">Set this field to zero.</span></span> <span data-ttu-id="c4644-109">Bei der Ausgabe gibt Netzwerkmonitor ein Handle für die-Eigenschaft zurück, nachdem die-Eigenschaft der Eigenschaften Datenbank hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4644-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="c4644-110">**Version**</span><span class="sxs-lookup"><span data-stu-id="c4644-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c4644-111">Reserved.</span></span> <span data-ttu-id="c4644-112">Muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c4644-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4644-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="c4644-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-114">Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4644-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="c4644-115">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="c4644-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-116">Die Beschreibung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4644-116">Description of the property.</span></span> <span data-ttu-id="c4644-117">Die Beschreibung wird auf der Netzwerkmonitor Statusleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4644-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="c4644-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="c4644-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-119">Datentyp der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4644-119">Data type of the property.</span></span> <span data-ttu-id="c4644-120">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c4644-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="c4644-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c4644-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="c4644-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4644-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="c4644-123"><dt>**Prop- \_ Typ \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="c4644-124">Der Eigenschaftentyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c4644-124">Property type is unknown.</span></span> <span data-ttu-id="c4644-125">Es gibt keine implizite Länge oder kein implizites Format.</span><span class="sxs-lookup"><span data-stu-id="c4644-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="c4644-126"><dt>**Prop \_ - \_ typzusammenfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="c4644-127">Eigenschaften Typen werden zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="c4644-127">Summarizing property type.</span></span> <span data-ttu-id="c4644-128">Gibt die erste Eigenschaften Instanz an, die der Parser an einen Frame anfügt.</span><span class="sxs-lookup"><span data-stu-id="c4644-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="c4644-129">Die \_ \_ Zusammenfassung des prop-Typs kann als Platzhalter für Gruppen von Eigenschaften dienen.</span><span class="sxs-lookup"><span data-stu-id="c4644-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="c4644-130">Dieser Wert gibt an, dass die Eigenschaft nicht im Protokoll *RFC* definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c4644-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="c4644-131"><dt>**Prop \_ - \_ typbyte**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="c4644-132">Numerische Daten mit einer Größe von einem Byte (8-Bit-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="c4644-133"><dt>**Prop \_ - \_ typwort**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="c4644-134">Numerische Daten mit einer Größe von zwei Bytes (16-Bit-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="c4644-135"><dt>**Prop- \_ Typ \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="c4644-136">Numerische Daten mit einer Größe von vier Bytes (32-Bit-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="c4644-137"><dt>**Prop- \_ Typ \_ largeint**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="c4644-138">Numerische Daten mit einer Größe von 8 Bytes (64-Bit-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="c4644-139"><dt>**Prop \_ Type \_ addr**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="c4644-140">Mac-Adresse (6-Byte-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="c4644-141"><dt>**Prop \_ - \_ typzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="c4644-142">**SYSTEMTIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c4644-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="c4644-143"><dt>**Prop \_ - \_ Zeichenfolge**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="c4644-144">ASCII-Textdaten.</span><span class="sxs-lookup"><span data-stu-id="c4644-144">ASCII text data.</span></span> <span data-ttu-id="c4644-145">Dieser Datentyp wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="c4644-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="c4644-146">Bei Unicode-Daten muss beim Aufrufen von ASCII-Textdaten auch das iflag- \_ Unicode-Flag festgelegt werden, wenn die Anfüge Eigenschaft-Instanzfunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4644-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="c4644-147"><dt>**\_ \_ IP-Adresse des prop-Typs \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="c4644-148">IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c4644-148">IP Address.</span></span> <span data-ttu-id="c4644-149">(4-Byte-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="c4644-150"><dt>**\_ \_ IPX- \_ Adresse des prop-Typs**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="c4644-151">IPX-Adresse</span><span class="sxs-lookup"><span data-stu-id="c4644-151">IPX Address.</span></span> <span data-ttu-id="c4644-152">(10-Byte-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="c4644-153"><dt>**"prop \_ Type \_ byteswlapp \_ Word"**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="c4644-154">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4644-154">Obsolete.</span></span> <span data-ttu-id="c4644-155">Legen Sie für Byte gesteuerte Word-Daten den **DataType** auf Prop \_ Type \_ Word fest, und legen Sie \_ beim Aufrufen einer **Anfüge** Eigenschaft-Instanzfunktion das eingetauschte iflag-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="c4644-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="c4644-156"><dt>**der prop- \_ Typ \_ byteswlapp \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="c4644-157">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4644-157">Obsolete.</span></span> <span data-ttu-id="c4644-158">Legen Sie für in Byte ausgelegte DWORD-Daten einen **DataType** -Wert auf Prop \_ Type \_ DWORD fest, und legen Sie \_ beim Aufrufen einer **Anfüge** Eigenschaft-Instanzfunktion das eingetauschte iflag fest.</span><span class="sxs-lookup"><span data-stu-id="c4644-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="c4644-159"><dt>**\_Typzeichenfolge für den Prop \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="c4644-160">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4644-160">Obsolete.</span></span> <span data-ttu-id="c4644-161">Legen Sie für Zeichen folgen Daten variabler Art **DataType** auf Prop \_ Type \_ String fest, und legen Sie das iflag Unicode-Flag fest, \_ Wenn Sie eine **Anfüge** Eigenschaften-Instanzfunktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4644-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="c4644-162"><dt>**Rohdaten des prop- \_ Typs \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="c4644-163">Rohdaten unbekannter Länge und Format.</span><span class="sxs-lookup"><span data-stu-id="c4644-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="c4644-164"><dt>**Prop \_ - \_ typkommentar**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="c4644-165">Identisch mit dem Prop- \_ Typ " \_ void".</span><span class="sxs-lookup"><span data-stu-id="c4644-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="c4644-166"><dt>**Prop- \_ Typ \_ srcfriendlyname**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="c4644-167">Adresse des Quell freundlichen namens.</span><span class="sxs-lookup"><span data-stu-id="c4644-167">Address of source-friendly name.</span></span> <span data-ttu-id="c4644-168">Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="c4644-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="c4644-169"><dt>**Prop- \_ Typ \_ dstfriendlyname**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="c4644-170">Adresse des Ziel anzeigen Amens.</span><span class="sxs-lookup"><span data-stu-id="c4644-170">Address of destination friendly name.</span></span> <span data-ttu-id="c4644-171">Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="c4644-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="c4644-172"><dt>**\_ \_ tokenringadresse des prop-Typs \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="c4644-173">Tokenringadresse.</span><span class="sxs-lookup"><span data-stu-id="c4644-173">Token-ring address.</span></span> <span data-ttu-id="c4644-174">Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="c4644-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="c4644-175"><dt>**Prop \_ Type-Adresse des Typs " \_ f" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="c4644-176">Die Adresse von "f".</span><span class="sxs-lookup"><span data-stu-id="c4644-176">FDDI address.</span></span> <span data-ttu-id="c4644-177">Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="c4644-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="c4644-178"><dt>**IP-Adresse des prop- \_ Typs \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="c4644-179">Ethernet-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c4644-179">Ethernet address.</span></span> <span data-ttu-id="c4644-180">Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="c4644-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="c4644-181"><dt>**\_ \_ Objekt \_ Bezeichner des prop-Typs**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="c4644-182">BER-codierter SNMP-Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c4644-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="c4644-183"><dt>**\_ \_ \_ IP-Adresse der prop-typreben \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="c4644-184">IP-Adresse der Reben (6-Byte-Entität).</span><span class="sxs-lookup"><span data-stu-id="c4644-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="c4644-185"><dt>**Prop \_ Type \_ var \_ len \_ Small \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="c4644-186">Numerischer Wert ohne vordefinierte Länge, aber nicht mehr als 8 Bytes.</span><span class="sxs-lookup"><span data-stu-id="c4644-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="c4644-187">Die Länge der angefügten Daten bestimmt die Länge des Werts.</span><span class="sxs-lookup"><span data-stu-id="c4644-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="c4644-188">**Dataqualifizierer**</span><span class="sxs-lookup"><span data-stu-id="c4644-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-189">Der Daten Qualifizierer einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4644-189">The data qualifier of a property.</span></span> <span data-ttu-id="c4644-190">Dieser Member stellt genaue Informationen zum Datentyp bereit.</span><span class="sxs-lookup"><span data-stu-id="c4644-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="c4644-191">**Dataqualifizierer** kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c4644-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="c4644-192">Wert</span><span class="sxs-lookup"><span data-stu-id="c4644-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="c4644-193">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4644-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="c4644-194"><dt>**Prop \_ Qual \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="c4644-195">Der-Eigenschafts Datentyp ist die einzige Spezifikation der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4644-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="c4644-196">Wenn dieser Wert festgelegt wird, wird der Union-Member der-Struktur auf **null** festgelegt und dann ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c4644-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="c4644-197"><dt>**Bereich für die Stütz \_ Qual \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="c4644-198">Es wird erwartet, dass der numerische Wert innerhalb eines angegebenen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="c4644-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="c4644-199">Definieren Sie den Bereich im **lprange** -Member.</span><span class="sxs-lookup"><span data-stu-id="c4644-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="c4644-200"><dt>**Prop- \_ Qual- \_ Satz**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="c4644-201">Der Wert einer Eigenschaft wird mit einem Satz von Werten verglichen, die im **lpset** -Member der Union-Struktur angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4644-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="c4644-202">Der Wert einer Eigenschaft kann ein **Byte**-, **Word**-, **DWORD**-, **largeint** -oder **time**-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="c4644-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="c4644-203"><dt>**Prop \_ - \_ Bitfeld**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="c4644-204">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4644-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="c4644-205"><dt>**Bezeichnung für "prop \_ Qual" \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="c4644-206">Der Wert einer Eigenschaft wird mit einem Wert in einem Satz von Wert Bezeichnungs Paaren verglichen.</span><span class="sxs-lookup"><span data-stu-id="c4644-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="c4644-207">Die Wert Bezeichnungs Paare werden im **lpset** -Member der Union-Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="c4644-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="c4644-208">Wenn der Wert der Eigenschaft zur Anzeigezeit mit einem Wert in der Menge übereinstimmt, werden sowohl ein Wert als auch die zugehörige Bezeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4644-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="c4644-209"><dt>**Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="c4644-210">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4644-210">Obsolete.</span></span> <span data-ttu-id="c4644-211">Verwenden Sie \_ stattdessen Prop-Qual- \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="c4644-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="c4644-212"><dt>**Prop \_ Qual \_ konstant**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="c4644-213">Der Wert einer Eigenschaft wird mit einer Konstante verglichen, die im **Wertmember** der Union angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4644-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="c4644-214">Wenn die Eigenschaftswerte und die Konstante nicht mit der Anzeigezeit identisch sind, wird eine formatierte Fehlermeldung angezeigt, und der Wert wird auf Normal festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4644-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="c4644-215"><dt>**Prop- \_ Qual- \_ Flags**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="c4644-216">Der Wert der-Eigenschaft wird mit bestimmten Bits verglichen, die im **lpset** -Member der Union identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c4644-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="c4644-217"><dt>**Prop- \_ Qual- \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="c4644-218">Der Wert einer Eigenschaft gibt ein Array von Werten an.</span><span class="sxs-lookup"><span data-stu-id="c4644-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="c4644-219">Die Länge der angefügten Daten bestimmt die Länge eines Arrays.</span><span class="sxs-lookup"><span data-stu-id="c4644-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="c4644-220">Wenn der Wert des prop \_ Qual \_ -Arrays festgelegt wird, wird das Unionmember der **PropertyInfo** -Datenstruktur auf **null** festgelegt und ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c4644-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="c4644-221">**lpextendedinfo**</span><span class="sxs-lookup"><span data-stu-id="c4644-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-222">Reserviert (Union-Mitglied).</span><span class="sxs-lookup"><span data-stu-id="c4644-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="c4644-223">**lprange**</span><span class="sxs-lookup"><span data-stu-id="c4644-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-224">Ein Zeiger auf eine [Bereichs](range.md) Struktur, die einen Wertebereich definiert.</span><span class="sxs-lookup"><span data-stu-id="c4644-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="c4644-225">Dieser Member muss festgelegt werden, wenn der **dataqualifier** -Member dieser Struktur auf den Prop-Wert \_ \_ Bereich (Member of Union) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4644-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="c4644-226">**lpset**</span><span class="sxs-lookup"><span data-stu-id="c4644-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-227">Ein Zeiger auf eine [Set](set.md) -Struktur, die einen Satz von Werten oder Bezeichnungen angibt.</span><span class="sxs-lookup"><span data-stu-id="c4644-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="c4644-228">Dieser Member muss festgelegt werden, wenn der **dataqualifier** -Member der Struktur auf Prop \_ Qual \_ Set, Prop \_ Qual \_ bezeichnete \_ Menge oder Prop \_ Qual \_ Flags (Member of Union) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4644-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="c4644-229">**Bitmaske**</span><span class="sxs-lookup"><span data-stu-id="c4644-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-230">Veraltet (Member der Union).</span><span class="sxs-lookup"><span data-stu-id="c4644-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="c4644-231">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c4644-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-232">Konstanter Wert, der verwendet wird, wenn **dataqualifizierer** auf Prop \_ Qual \_ konstant (Member of Union) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4644-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="c4644-233">**Formatstringsize**</span><span class="sxs-lookup"><span data-stu-id="c4644-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-234">Maximale Größe, die nur für die Eigenschafts Beschreibung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4644-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="c4644-235">**InstanceData**</span><span class="sxs-lookup"><span data-stu-id="c4644-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="c4644-236">Geben Sie die Format Funktion an, die zum Formatieren der angezeigten Daten für die Eigenschaft aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4644-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="c4644-237">Wenn Sie den generischen Formatierer verwenden möchten, geben Sie die **formatpropertyinstance** -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="c4644-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4644-238">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4644-238">Remarks</span></span>

<span data-ttu-id="c4644-239">Die **PropertyInfo** -Struktur wird in Aufrufen der [AddProperty](/previous-versions/bb251873(v=msdn.10)) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4644-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="c4644-240">Die **AddProperty** -Funktion fügt der Parser- [*Eigenschaften Datenbank*](p.md)eine einzelne Eigenschafts Definition hinzu.</span><span class="sxs-lookup"><span data-stu-id="c4644-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4644-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4644-241">Requirements</span></span>



| <span data-ttu-id="c4644-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4644-242">Requirement</span></span> | <span data-ttu-id="c4644-243">Wert</span><span class="sxs-lookup"><span data-stu-id="c4644-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c4644-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4644-244">Minimum supported client</span></span><br/> | <span data-ttu-id="c4644-245">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4644-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c4644-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4644-246">Minimum supported server</span></span><br/> | <span data-ttu-id="c4644-247">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4644-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c4644-248">Header</span><span class="sxs-lookup"><span data-stu-id="c4644-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4644-249"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4644-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4644-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4644-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4644-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c4644-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="c4644-252">Bereich</span><span class="sxs-lookup"><span data-stu-id="c4644-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="c4644-253">SET</span><span class="sxs-lookup"><span data-stu-id="c4644-253">SET</span></span>](set.md)
</dt> </dl>

 

