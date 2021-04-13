---
description: Fungiert als übergeordnete Klasse für Klassen, die zum Registrieren von Klassen-und instanzanbietern in WMI verwendet werden.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: __ObjectProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345899"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="d1dc2-103">\_\_Objectproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1dc2-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="d1dc2-104">Die abstrakte System Klasse **\_ \_ objectproviderregistration** fungiert als übergeordnete Klasse für Klassen, die zum Registrieren von Klassen-und instanzanbietern in WMI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="d1dc2-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1dc2-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1dc2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1dc2-107">Syntax</span></span>

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="d1dc2-108">Member</span><span class="sxs-lookup"><span data-stu-id="d1dc2-108">Members</span></span>

<span data-ttu-id="d1dc2-109">Die **\_ \_ objectproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d1dc2-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="d1dc2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1dc2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1dc2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1dc2-111">Properties</span></span>

<span data-ttu-id="d1dc2-112">Die **\_ \_ objectproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1dc2-113">**Interaktionstyp**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-114">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-116">Gibt an, ob der Klassen-oder Instanzanbieter seine eigenen Daten bereitstellt, oder stützt sich auf WMI und das Common Information Model (CIM)-Repository.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="d1dc2-117">Pull-Anbieter unterstützen den dynamischen Zugriff auf Ihre Daten, und pushanbieter speichern Ihre Daten im CIM-Repository und basieren auf WMI, um Zugriff darauf zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="d1dc2-118">Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="d1dc2-119">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="d1dc2-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="d1dc2-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d1dc2-121">Der Anbieter ist ein Pull-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="d1dc2-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="d1dc2-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d1dc2-123">Der Anbieter ist ein Push-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="d1dc2-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Pushverify** (2)</span><span class="sxs-lookup"><span data-stu-id="d1dc2-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d1dc2-125">Der Anbieter ist ein Push-Verify-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="d1dc2-126">Beachten Sie, dass Push-Verify zurzeit nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1dc2-127">**ab**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-128">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1dc2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-130">Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die einen Objekt Pfad zum Objekt Anbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="d1dc2-131">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-132">**Querysupportlevels**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d1dc2-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-135">Array der Typen der Anbieter bezogenen Unterstützung für die Abfrage Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="d1dc2-136">Klassen Anbieter unterstützen keine Typen von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="d1dc2-137">Instanzanbieter können **querysupportlevels** auf **null** festlegen, wenn Sie die Abfrage Verarbeitung nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="d1dc2-138">Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode, und legen Sie diese Eigenschaft auf einen oder mehrere der folgenden Werte fest (der Eigenschaftentyp ist ein Array).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="d1dc2-139">"WQL: unaryselect"</span><span class="sxs-lookup"><span data-stu-id="d1dc2-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="d1dc2-140">"WQL: Verweise"</span><span class="sxs-lookup"><span data-stu-id="d1dc2-140">"WQL:References"</span></span>

<span data-ttu-id="d1dc2-141">"WQL: assoziatoren"</span><span class="sxs-lookup"><span data-stu-id="d1dc2-141">"WQL:Associators"</span></span>

<span data-ttu-id="d1dc2-142">"WQL: V1ProviderDefined"</span><span class="sxs-lookup"><span data-stu-id="d1dc2-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-143">**Supportsbatching**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-146">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-150">**True** gibt an, dass der Anbieter das Löschen von Daten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="d1dc2-151">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1dc2-151">True</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-152">Der Anbieter unterstützt das Löschen von Klassen oder Instanzen durch Implementieren eines der beiden folgenden [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassen Anbieter) oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-153">False</span><span class="sxs-lookup"><span data-stu-id="d1dc2-153">False</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-154">Der Anbieter unterstützt keine Daten Löschung und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) oder [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1dc2-155">**Supportsenumeration**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-156">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-158">**True** gibt an, dass der Anbieter datenenumeration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="d1dc2-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1dc2-159">True</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-160">Der Anbieter unterstützt die datenenumeration durch Implementieren eines der beiden Typen [**IWbemServices:: | ateclassenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (Klassen Anbieter) oder [**IWbemServices:: feateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (Instanzanbieter).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-161">False</span><span class="sxs-lookup"><span data-stu-id="d1dc2-161">False</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-162">Der Anbieter unterstützt keine datenenumeration und gibt [](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)den **WBEM \_ E- \_ Anbieter \_ \_** zurück, [**der**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) nicht in der Lage ist, von "" aus "", "", "", "", "", ""</span><span class="sxs-lookup"><span data-stu-id="d1dc2-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1dc2-163">**Supportsget**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-164">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-166">**True** gibt an, dass der Klassen-oder Instanzanbieter den Datenabruf unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="d1dc2-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1dc2-167">True</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-168">Der Anbieter unterstützt den Datenabruf durch Implementieren von [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-169">False</span><span class="sxs-lookup"><span data-stu-id="d1dc2-169">False</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-170">Der Anbieter unterstützt nicht das Abrufen von Daten und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1dc2-171">**Supportsput**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-174">**True** gibt an, dass der Klassen-oder Instanzanbieter die Datenänderung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="d1dc2-175">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1dc2-175">True</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-176">Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren eines der beiden [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="d1dc2-177">False</span><span class="sxs-lookup"><span data-stu-id="d1dc2-177">False</span></span>
</dt> <dd>

<span data-ttu-id="d1dc2-178">Der Anbieter unterstützt keine Datenänderungen und gibt den **WBEM E-Anbieter zurück, der \_ nicht \_ \_ \_** von [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) oder [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1dc2-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1dc2-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1dc2-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d1dc2-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1dc2-182">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1dc2-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1dc2-183">Remarks</span></span>

<span data-ttu-id="d1dc2-184">Die **\_ \_ objectproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="d1dc2-185">Klassen Anbieter müssen die **supportsenumeration** -Eigenschaft auf **true** festlegen, da die Anbieter in der Lage sein müssen, WMI mit einer Liste Ihrer Klassen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="d1dc2-186">Wenn ein Klassen Anbieter versucht, diese Eigenschaft auf **false** festzulegen, wird die Registrierung von WMI als unzulässig gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="d1dc2-187">Instanzanbieter müssen die Enumeration nicht unterstützen, und Sie können festlegen, dass **supportsenumeration** auf " **true** " oder " **false**" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="d1dc2-188">Ein Anbieter, der **querysupportlevels** auf "WQL: unaryselect" festlegt, kann eine Abfrage akzeptieren, die aus der grundlegenden SELECT-Anweisung besteht, wie in WMI-Version 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="d1dc2-189">Es wird erwartet, dass sowohl Klassen-als auch Instanzanbieter die **\_ \_ Klassen** System Eigenschaft verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="d1dc2-190">Klassen Anbieter werden außerdem erwartet, dass die System Eigenschaft " **\_ \_ Superclass** " und der ISA-Operator verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="d1dc2-191">Der ISA-Operator wird verwendet, um ein Resultset auf abgeleitete Klassen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="d1dc2-192">Wenn ein Anbieter eine Abfrage erhält, die er nicht interpretieren kann, fordert er an, dass WMI ihn verarbeitet, indem er den Fehlerwert **WBEM \_ E \_ zu \_ Komplex** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="d1dc2-193">Eine Beschreibung der gültigen WQL-Syntax finden Sie unter [Querying with WQL (Abfragen mit WQL](querying-with-wql.md)).</span><span class="sxs-lookup"><span data-stu-id="d1dc2-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="d1dc2-194">Ein Anbieter, der **querysupportlevels** auf **WQL: V1ProviderDefined** festlegt, kann versuchen, eine größere Menge der SQL-Syntax zu unterstützen, z. b `ORDER BY` . die-Klausel.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="d1dc2-195">WMI interpretiert die zusätzlichen Klauseln nicht, oder es wird versucht, sicherzustellen, dass das Resultset korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="d1dc2-196">Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) erstellen und registrieren.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1dc2-197">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1dc2-197">Requirements</span></span>



| <span data-ttu-id="d1dc2-198">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1dc2-198">Requirement</span></span> | <span data-ttu-id="d1dc2-199">Wert</span><span class="sxs-lookup"><span data-stu-id="d1dc2-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d1dc2-200">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1dc2-200">Minimum supported client</span></span><br/> | <span data-ttu-id="d1dc2-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1dc2-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d1dc2-202">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1dc2-202">Minimum supported server</span></span><br/> | <span data-ttu-id="d1dc2-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1dc2-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d1dc2-204">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1dc2-204">Namespace</span></span><br/>                | <span data-ttu-id="d1dc2-205">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="d1dc2-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d1dc2-206">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1dc2-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1dc2-207">**\_\_Providerregistration**</span><span class="sxs-lookup"><span data-stu-id="d1dc2-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="d1dc2-208">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="d1dc2-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d1dc2-209">Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="d1dc2-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

