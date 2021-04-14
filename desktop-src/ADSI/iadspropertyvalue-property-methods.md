---
title: Iadspropertyvalue-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadspropertyvalue-Schnittstelle ermöglichen den Zugriff auf die in der folgenden Tabelle beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- Iadspropertyvalue-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476353"
---
# <a name="iadspropertyvalue-property-methods"></a><span data-ttu-id="d6c79-105">Iadspropertyvalue-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="d6c79-105">IADsPropertyValue Property Methods</span></span>

<span data-ttu-id="d6c79-106">Die Eigenschaften Methoden der [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) -Schnittstelle ermöglichen den Zugriff auf die in der folgenden Tabelle beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d6c79-106">The property methods of the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface provide access to the properties described in the following table.</span></span> <span data-ttu-id="d6c79-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d6c79-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d6c79-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6c79-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d6c79-109">**Adstype**</span><span class="sxs-lookup"><span data-stu-id="d6c79-109">**ADsType**</span></span>
<span data-ttu-id="d6c79-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-111">Der Datentyp des Werts der Eigenschaft, die aus der [**adstypeer**](/windows/win32/api/iads/ne-iads-adstypeenum) -Enumeration entnommen wurde, der Value-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d6c79-111">The data type of the value of the property, taken from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration, of the value property.</span></span>

<dt>

<span data-ttu-id="d6c79-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="d6c79-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-114">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d6c79-114">**Boolean**</span></span>
<span data-ttu-id="d6c79-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-116">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="d6c79-116">Boolean value.</span></span>

<dt>

<span data-ttu-id="d6c79-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="d6c79-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-119">**Caseexactstring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-119">**CaseExactString**</span></span>
<span data-ttu-id="d6c79-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-121">Zu interpretierende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d6c79-121">String to be interpreted.</span></span> <span data-ttu-id="d6c79-122">Groß-/Kleinschreibung wird beachtet,</span><span class="sxs-lookup"><span data-stu-id="d6c79-122">Case-sensitive.</span></span>

<dt>

<span data-ttu-id="d6c79-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-124">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6c79-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-125">**Caseignorestring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-125">**CaseIgnoreString**</span></span>
<span data-ttu-id="d6c79-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-127">Zu interpretierende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d6c79-127">String to be interpreted.</span></span> <span data-ttu-id="d6c79-128">Diese Klasse berücksichtigt keine Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d6c79-128">Case insensitive.</span></span>

<dt>

<span data-ttu-id="d6c79-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-130">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6c79-130">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-131">**Dnstring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-131">**DNString**</span></span>
<span data-ttu-id="d6c79-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-133">Eine Zeichenfolge, die den Distinguished Name (Pfad) eines Verzeichnisdienst-Wert Objekts bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d6c79-133">String that identifies the distinguished name (path) of a directory service value object.</span></span>

<dt>

<span data-ttu-id="d6c79-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-135">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6c79-135">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-136">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d6c79-136">**Integer**</span></span>
<span data-ttu-id="d6c79-137"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-137"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-138">Wert für ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="d6c79-138">Integer value.</span></span>

<dt>

<span data-ttu-id="d6c79-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-140">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="d6c79-140">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-141">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="d6c79-141">**LargeInteger**</span></span>
<span data-ttu-id="d6c79-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-143">Ein Zeiger auf die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle des Objekts, das [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) für diesen Wert implementiert.</span><span class="sxs-lookup"><span data-stu-id="d6c79-143">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) for this value.</span></span>

<dt>

<span data-ttu-id="d6c79-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-145">Skript Datentyp: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d6c79-145">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-146">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="d6c79-146">**NumericString**</span></span>
<span data-ttu-id="d6c79-147"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-147"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-148">Text, der interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6c79-148">Text to be interpreted.</span></span> <span data-ttu-id="d6c79-149">Numerischer Typ.</span><span class="sxs-lookup"><span data-stu-id="d6c79-149">Numeric type.</span></span>

<dt>

<span data-ttu-id="d6c79-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-151">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6c79-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-152">**Octetstring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-152">**OctetString**</span></span>
<span data-ttu-id="d6c79-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-154">Variant-Array von 1-Byte-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d6c79-154">Variant array of one-byte characters.</span></span>

<dt>

<span data-ttu-id="d6c79-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-156">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="d6c79-156">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-157">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="d6c79-157">**PrintableString**</span></span>
<span data-ttu-id="d6c79-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-159">Anzeige-oder Druck Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d6c79-159">Display or print string.</span></span>

<dt>

<span data-ttu-id="d6c79-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-161">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6c79-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-162">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d6c79-162">**SecurityDescriptor**</span></span>
<span data-ttu-id="d6c79-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-164">Ein Zeiger auf die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle des Objekts, das [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) für diesen Wert implementiert.</span><span class="sxs-lookup"><span data-stu-id="d6c79-164">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) for this value.</span></span>

<dt>

<span data-ttu-id="d6c79-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-166">Skript Datentyp: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d6c79-166">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c79-167">**UtcTime**</span><span class="sxs-lookup"><span data-stu-id="d6c79-167">**UTCTime**</span></span>
<span data-ttu-id="d6c79-168"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d6c79-168"></dt> <dd> <dl></span></span>

<span data-ttu-id="d6c79-169">Ein Datum des **VT- \_ Datentyps** , ausgedrückt im UTC-Format (koordinierte Weltzeit).</span><span class="sxs-lookup"><span data-stu-id="d6c79-169">A date of the **VT\_DATE** type expressed in Coordinated Universal Time (UTC) format.</span></span>

<dt>

<span data-ttu-id="d6c79-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6c79-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d6c79-171">Skript Datentyp: **Datum**</span><span class="sxs-lookup"><span data-stu-id="d6c79-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="d6c79-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6c79-172">Remarks</span></span>

<span data-ttu-id="d6c79-173">Mit den [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) -Eigenschaften wird nur ein Eigenschafts Wert des angegebenen Typs festgelegt oder abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d6c79-173">The [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) properties will only set or retrieve a property value of the specified type.</span></span> <span data-ttu-id="d6c79-174">Beispielsweise führt die **caseignorestring** -Eigenschaft eines Attributs vom Typ **adstype \_ DN \_ String**, wie **das Attribut** "das Attribut" ", zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="d6c79-174">For example, the **CaseIgnoreString** property on an attribute of type **ADSTYPE\_DN\_STRING**, like the **distinguishedName** attribute, will result in an error.</span></span> <span data-ttu-id="d6c79-175">Die **caseignorestring** -Eigenschaft funktioniert nur bei Attributen vom Typ ADS-Schreibweise **\_ \_ \_ Zeichenfolge ignorieren**.</span><span class="sxs-lookup"><span data-stu-id="d6c79-175">The **CaseIgnoreString** property will only work on attributes of type **ADS\_CASE\_IGNORE\_STRING**.</span></span> <span data-ttu-id="d6c79-176">In der folgenden Tabelle wird der [**adstyperenum**](/windows/win32/api/iads/ne-iads-adstypeenum) -Wert der entsprechenden **iadspropertyvalue** -Eigenschaft zugeordnet, die für den Zugriff auf diesen Attributtyp verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6c79-176">The following table maps the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value to the corresponding **IADsPropertyValue** property that can be used to access that attribute type.</span></span> <span data-ttu-id="d6c79-177">Wenn ein **adstypum** -Wert in dieser Tabelle nicht aufgeführt ist, ist er nicht über die **iadspropertyvalue** -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6c79-177">If an **ADSTYPEENUM** value is not listed in this table, it is not available from the **IADsPropertyValue** interface.</span></span> <span data-ttu-id="d6c79-178">Die [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) -Schnittstelle sollte zum Abrufen von Daten in den anderen Formaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6c79-178">The [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interface should be used to obtain data in the other formats.</span></span>



| <span data-ttu-id="d6c79-179">[**Adstypum**](/windows/win32/api/iads/ne-iads-adstypeenum) -Wert</span><span class="sxs-lookup"><span data-stu-id="d6c79-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value</span></span> | <span data-ttu-id="d6c79-180">[**Iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d6c79-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) property</span></span> |
|------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d6c79-181">**adstype- \_ DN- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6c79-181">**ADSTYPE\_DN\_STRING**</span></span>                  | <span data-ttu-id="d6c79-182">**Dnstring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-182">**DNString**</span></span>                                            |
| <span data-ttu-id="d6c79-183">**exakte Groß-/Kleinschreibung von adstype \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c79-183">**ADSTYPE\_CASE\_EXACT\_STRING**</span></span>         | <span data-ttu-id="d6c79-184">**Caseexactstring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-184">**CaseExactString**</span></span>                                     |
| <span data-ttu-id="d6c79-185">**adstype \_ Case \_ - \_ Zeichenfolge ignorieren**</span><span class="sxs-lookup"><span data-stu-id="d6c79-185">**ADSTYPE\_CASE\_IGNORE\_STRING**</span></span>        | <span data-ttu-id="d6c79-186">**Caseignorestring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-186">**CaseIgnoreString**</span></span>                                    |
| <span data-ttu-id="d6c79-187">**Druckbare adstype- \_ \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6c79-187">**ADSTYPE\_PRINTABLE\_STRING**</span></span>           | <span data-ttu-id="d6c79-188">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="d6c79-188">**PrintableString**</span></span>                                     |
| <span data-ttu-id="d6c79-189">**\_numerische \_ Zeichenfolge von adstype**</span><span class="sxs-lookup"><span data-stu-id="d6c79-189">**ADSTYPE\_NUMERIC\_STRING**</span></span>             | <span data-ttu-id="d6c79-190">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="d6c79-190">**NumericString**</span></span>                                       |
| <span data-ttu-id="d6c79-191">**boolescher Wert von adstype \_**</span><span class="sxs-lookup"><span data-stu-id="d6c79-191">**ADSTYPE\_BOOLEAN**</span></span>                     | <span data-ttu-id="d6c79-192">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d6c79-192">**Boolean**</span></span>                                             |
| <span data-ttu-id="d6c79-193">**adstype- \_ Ganzzahl**</span><span class="sxs-lookup"><span data-stu-id="d6c79-193">**ADSTYPE\_INTEGER**</span></span>                     | <span data-ttu-id="d6c79-194">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d6c79-194">**Integer**</span></span>                                             |
| <span data-ttu-id="d6c79-195">**Zeichenfolge des adstype- \_ Oktetts \_**</span><span class="sxs-lookup"><span data-stu-id="d6c79-195">**ADSTYPE\_OCTET\_STRING**</span></span>               | <span data-ttu-id="d6c79-196">**Octetstring**</span><span class="sxs-lookup"><span data-stu-id="d6c79-196">**OctetString**</span></span>                                         |
| <span data-ttu-id="d6c79-197">**adstype- \_ UTC- \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="d6c79-197">**ADSTYPE\_UTC\_TIME**</span></span>                   | <span data-ttu-id="d6c79-198">**UtcTime**</span><span class="sxs-lookup"><span data-stu-id="d6c79-198">**UTCTime**</span></span>                                             |
| <span data-ttu-id="d6c79-199">**\_hohe Ganzzahl von adstype \_**</span><span class="sxs-lookup"><span data-stu-id="d6c79-199">**ADSTYPE\_LARGE\_INTEGER**</span></span>              | <span data-ttu-id="d6c79-200">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="d6c79-200">**LargeInteger**</span></span>                                        |
| <span data-ttu-id="d6c79-201">**adstype \_ NT- \_ Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6c79-201">**ADSTYPE\_NT\_SECURITY\_DESCRIPTOR**</span></span>    | <span data-ttu-id="d6c79-202">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d6c79-202">**SecurityDescriptor**</span></span>                                  |



 

## <a name="examples"></a><span data-ttu-id="d6c79-203">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6c79-203">Examples</span></span>

<span data-ttu-id="d6c79-204">Im folgenden Codebeispiel wird gezeigt, wie eine Eigenschaft aus der Eigenschaften Liste abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d6c79-204">The following code example shows how to retrieve a property from the property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="d6c79-205">Der folgende Code zeigt, wie **iadspropertyvalue:: get \_ caseignorestring** verwendet wird, um den Wert der Description-Eigenschaft aus einer Eigenschaften Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6c79-205">The following code shows how to use **IADsPropertyValue::get\_CaseIgnoreString** to retrieve the value of the description property from a property list.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="d6c79-206">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6c79-206">Requirements</span></span>



| <span data-ttu-id="d6c79-207">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6c79-207">Requirement</span></span> | <span data-ttu-id="d6c79-208">Wert</span><span class="sxs-lookup"><span data-stu-id="d6c79-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c79-209">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6c79-209">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c79-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6c79-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6c79-211">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6c79-211">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c79-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6c79-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6c79-213">Header</span><span class="sxs-lookup"><span data-stu-id="d6c79-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c79-214"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c79-214"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d6c79-215">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c79-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6c79-216"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6c79-216"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6c79-217">IID</span><span class="sxs-lookup"><span data-stu-id="d6c79-217">IID</span></span><br/>                      | <span data-ttu-id="d6c79-218">IID \_ iadspropertyvalue ist als 79fa9ad0-a97c-11D0-8534-00c04sd8d503 definiert.</span><span class="sxs-lookup"><span data-stu-id="d6c79-218">IID\_IADsPropertyValue is defined as 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="d6c79-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6c79-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c79-220">**Iadspropertyvalue**</span><span class="sxs-lookup"><span data-stu-id="d6c79-220">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="d6c79-221">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="d6c79-221">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="d6c79-222">**Iadspropertyentry**</span><span class="sxs-lookup"><span data-stu-id="d6c79-222">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="d6c79-223">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="d6c79-223">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="d6c79-224">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="d6c79-224">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="d6c79-225">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d6c79-225">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="d6c79-226">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d6c79-226">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

