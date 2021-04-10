---
description: Die CIM \_ supportaccess-Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: CIM_SupportAccess-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126872"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="48334-103">CIM- \_ supportaccess-Klasse</span><span class="sxs-lookup"><span data-stu-id="48334-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="48334-104">Die **CIM \_ supportaccess** -Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="48334-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48334-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48334-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48334-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="48334-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48334-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48334-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="48334-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="48334-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48334-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="48334-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="48334-110">Member</span><span class="sxs-lookup"><span data-stu-id="48334-110">Members</span></span>

<span data-ttu-id="48334-111">Die **CIM- \_ supportaccess** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48334-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="48334-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48334-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48334-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48334-113">Properties</span></span>

<span data-ttu-id="48334-114">Die **CIM- \_ supportaccess** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48334-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48334-115">**Communicationinfo**</span><span class="sxs-lookup"><span data-stu-id="48334-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48334-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48334-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48334-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48334-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48334-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,11 "," MIF. DMTF \| FRU \| 002,12 ")</span><span class="sxs-lookup"><span data-stu-id="48334-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="48334-119">Details zum Kommunikationsmodus.</span><span class="sxs-lookup"><span data-stu-id="48334-119">Details of the communication mode.</span></span> <span data-ttu-id="48334-120">Wenn die **communicationmode** -Eigenschaft z. b. "Phone" ist, gibt diese Eigenschaft die Telefonnummer an, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="48334-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="48334-121">**Communicationmode**</span><span class="sxs-lookup"><span data-stu-id="48334-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48334-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48334-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48334-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48334-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48334-124">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Unterstützung \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="48334-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="48334-125">Form der Kommunikation, die zum Abrufen von Support verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48334-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48334-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="48334-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="48334-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Telefon** (2)</span><span class="sxs-lookup"><span data-stu-id="48334-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="48334-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span><span class="sxs-lookup"><span data-stu-id="48334-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="48334-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span><span class="sxs-lookup"><span data-stu-id="48334-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="48334-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Dienst** (5)</span><span class="sxs-lookup"><span data-stu-id="48334-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="48334-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Webseite** (6)</span><span class="sxs-lookup"><span data-stu-id="48334-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="48334-132">Webseite</span><span class="sxs-lookup"><span data-stu-id="48334-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="48334-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span><span class="sxs-lookup"><span data-stu-id="48334-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="48334-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-Mail** (8)</span><span class="sxs-lookup"><span data-stu-id="48334-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="48334-135">Email</span><span class="sxs-lookup"><span data-stu-id="48334-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48334-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48334-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48334-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48334-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48334-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48334-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48334-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Unterstützung \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="48334-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="48334-140">Textbeschreibung des angegebenen Unterstützungs Typs.</span><span class="sxs-lookup"><span data-stu-id="48334-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="48334-141">**Gebietsschema**</span><span class="sxs-lookup"><span data-stu-id="48334-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48334-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48334-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48334-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48334-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48334-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Unterstützung \| 001,2 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="48334-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="48334-145">Geografische Region oder sprach Dialekt, auf den sich diese Ressource bezieht.</span><span class="sxs-lookup"><span data-stu-id="48334-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="48334-146">**SupportAccessID**</span><span class="sxs-lookup"><span data-stu-id="48334-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48334-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48334-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48334-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48334-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48334-149">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="48334-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48334-150">Eine beliebige frei Form Zeichenfolge, die vom Produkthersteller oder von der Organisation definiert wird, die das Produkt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="48334-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="48334-151">Diese Eigenschaft, da es sich um einen Schlüssel handelt, sollte im gesamten Unternehmen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="48334-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48334-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48334-152">Remarks</span></span>

<span data-ttu-id="48334-153">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="48334-153">WMI does not implement this class.</span></span>

<span data-ttu-id="48334-154">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="48334-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48334-155">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="48334-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48334-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48334-156">Requirements</span></span>



| <span data-ttu-id="48334-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48334-157">Requirement</span></span> | <span data-ttu-id="48334-158">Wert</span><span class="sxs-lookup"><span data-stu-id="48334-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48334-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48334-159">Minimum supported client</span></span><br/> | <span data-ttu-id="48334-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48334-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48334-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48334-161">Minimum supported server</span></span><br/> | <span data-ttu-id="48334-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48334-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48334-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="48334-163">Namespace</span></span><br/>                | <span data-ttu-id="48334-164">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="48334-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48334-165">MOF</span><span class="sxs-lookup"><span data-stu-id="48334-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48334-166"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48334-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48334-167">DLL</span><span class="sxs-lookup"><span data-stu-id="48334-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48334-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48334-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

