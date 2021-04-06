---
description: Registriert Klassen Anbieter in WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: __ClassProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
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
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760459"
---
# <a name="__classproviderregistration-class"></a><span data-ttu-id="47855-103">\_\_Classproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="47855-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="47855-104">Die **\_ \_ classproviderregistration** -System Klasse registriert Klassen Anbieter in WMI.</span><span class="sxs-lookup"><span data-stu-id="47855-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="47855-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="47855-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="47855-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="47855-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47855-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47855-107">Syntax</span></span>

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a><span data-ttu-id="47855-108">Member</span><span class="sxs-lookup"><span data-stu-id="47855-108">Members</span></span>

<span data-ttu-id="47855-109">Die **\_ \_ classproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47855-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="47855-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47855-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47855-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47855-111">Properties</span></span>

<span data-ttu-id="47855-112">Die **\_ \_ classproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47855-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47855-113">**CacheRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="47855-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-114">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="47855-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="47855-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47855-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="47855-117">**Interaktionstyp**</span><span class="sxs-lookup"><span data-stu-id="47855-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47855-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47855-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-120">Gibt an, ob der Klassen-oder Instanzanbieter Daten bereitstellt, oder ob er sich auf WMI und das Common Information Model (CIM)-Repository stützt.</span><span class="sxs-lookup"><span data-stu-id="47855-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="47855-121">Pull-Anbieter unterstützen den dynamischen Zugriff auf Daten, und pushanbieter speichern Daten im CIM-Repository und basieren auf WMI, um Zugriff darauf zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="47855-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="47855-122">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="47855-122">The default value is 0 (zero).</span></span> <span data-ttu-id="47855-123">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="47855-124">Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="47855-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="47855-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="47855-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="47855-126">Der Anbieter ist ein Pull-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="47855-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="47855-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="47855-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="47855-128">Der Anbieter ist ein Push-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="47855-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="47855-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Pushverify** (2)</span><span class="sxs-lookup"><span data-stu-id="47855-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="47855-130">Der Anbieter ist ein Push-Verify-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="47855-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="47855-131">Beachten Sie, dass **pushverify** -Anbieter zurzeit nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="47855-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47855-132">**Peruserschema**</span><span class="sxs-lookup"><span data-stu-id="47855-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-135">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47855-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="47855-136">**ab**</span><span class="sxs-lookup"><span data-stu-id="47855-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-137">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="47855-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="47855-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47855-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47855-139">Objekt Pfad zu einem Klassen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="47855-139">Object path to a class provider.</span></span> <span data-ttu-id="47855-140">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="47855-141">**Querysupportlevels**</span><span class="sxs-lookup"><span data-stu-id="47855-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-142">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="47855-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="47855-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-144">Array der Typen der Anbieter bezogenen Unterstützung für die Abfrage Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="47855-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="47855-145">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="47855-146">Klassen Anbieter sind erforderlich, um mindestens einen Abfragetyp zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="47855-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="47855-147">Instanzanbieter können **querysupportlevels** auf **null** festlegen, wenn Sie die Abfrage Verarbeitung nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="47855-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="47855-148">Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode, und legen Sie diese Eigenschaft auf einen oder mehrere der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="47855-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="47855-149">("WQL: unaryselect")</span><span class="sxs-lookup"><span data-stu-id="47855-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="47855-150">("WQL: Verweise")</span><span class="sxs-lookup"><span data-stu-id="47855-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="47855-151">("WQL: assoziatoren")</span><span class="sxs-lookup"><span data-stu-id="47855-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="47855-152">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="47855-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="47855-153">**Referencedsetqueries**</span><span class="sxs-lookup"><span data-stu-id="47855-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-154">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="47855-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="47855-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-156">Eine oder mehrere Abfragen, die den Satz der referenzierten Klassen beschreiben, die von einem Klassen Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="47855-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="47855-157">Anbieter, die Zuordnungs Klassen bereitstellen können, müssen mindestens eine Abfrage in diese Eigenschaft einschließen.</span><span class="sxs-lookup"><span data-stu-id="47855-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="47855-158">**Resultsetqueries**</span><span class="sxs-lookup"><span data-stu-id="47855-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-159">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="47855-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="47855-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-161">Eine oder mehrere Abfragen, die den Satz aller Klassen beschreiben, die vom Klassen Anbieter bereitgestellt werden können, oder eine übergeordnete Gruppe dieser Klassen.</span><span class="sxs-lookup"><span data-stu-id="47855-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="47855-162">Diese Eigenschaft gibt nie eine Teilmenge der unterstützten Klassen an.</span><span class="sxs-lookup"><span data-stu-id="47855-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="47855-163">**Resynchronisierung-namespaceopen**</span><span class="sxs-lookup"><span data-stu-id="47855-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-164">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-166">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47855-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="47855-167">**Supportsbatching**</span><span class="sxs-lookup"><span data-stu-id="47855-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-170">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47855-170">Not used.</span></span>

<span data-ttu-id="47855-171">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="47855-172">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="47855-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-173">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-175">**True** gibt an, dass der Anbieter das Löschen von Daten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47855-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="47855-176">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="47855-177">Fall</span><span class="sxs-lookup"><span data-stu-id="47855-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="47855-178">Der Anbieter unterstützt das Löschen von Klassen oder Instanzen durch Implementieren eines der beiden folgenden [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassen Anbieter) oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter).</span><span class="sxs-lookup"><span data-stu-id="47855-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="47855-179">Alarm</span><span class="sxs-lookup"><span data-stu-id="47855-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="47855-180">Der Anbieter unterstützt keine Daten Löschung und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) oder [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47855-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47855-181">**Supportsenumeration**</span><span class="sxs-lookup"><span data-stu-id="47855-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-182">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-183">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-184">**True** gibt an, dass der Anbieter datenenumeration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47855-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="47855-185">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="47855-186">Fall</span><span class="sxs-lookup"><span data-stu-id="47855-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="47855-187">Der Anbieter unterstützt die datenenumeration durch Implementieren eines der beiden Typen [**IWbemServices:: | ateclassenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (Klassen Anbieter) oder [**IWbemServices:: feateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (Instanzanbieter).</span><span class="sxs-lookup"><span data-stu-id="47855-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="47855-188">Alarm</span><span class="sxs-lookup"><span data-stu-id="47855-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="47855-189">Der Anbieter unterstützt keine datenenumeration und gibt [](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)den **WBEM \_ E- \_ Anbieter \_ \_** zurück, [**der**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) nicht in der Lage ist, von "" aus "", "", "", "", "", ""</span><span class="sxs-lookup"><span data-stu-id="47855-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47855-190">**Supportsget**</span><span class="sxs-lookup"><span data-stu-id="47855-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-191">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-193">**True** gibt an, dass der Klassen-oder Instanzanbieter den Datenabruf unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47855-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="47855-194">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="47855-195">Fall</span><span class="sxs-lookup"><span data-stu-id="47855-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="47855-196">Der Anbieter unterstützt den Datenabruf durch Implementieren von [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="47855-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="47855-197">Alarm</span><span class="sxs-lookup"><span data-stu-id="47855-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="47855-198">Der Anbieter unterstützt nicht das Abrufen von Daten und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47855-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47855-199">**Supportsput**</span><span class="sxs-lookup"><span data-stu-id="47855-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-200">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-201">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-202">**True** gibt an, dass der Klassen-oder Instanzanbieter die Datenänderung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47855-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="47855-203">Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="47855-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="47855-204">Fall</span><span class="sxs-lookup"><span data-stu-id="47855-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="47855-205">Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren eines der beiden [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter).</span><span class="sxs-lookup"><span data-stu-id="47855-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="47855-206">Alarm</span><span class="sxs-lookup"><span data-stu-id="47855-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="47855-207">Der Anbieter unterstützt keine Datenänderungen und gibt den **WBEM E-Anbieter zurück, der \_ nicht \_ \_ \_** von [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) oder [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47855-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47855-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="47855-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-209">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-210">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-211">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47855-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="47855-212">**Suppportsbatching**</span><span class="sxs-lookup"><span data-stu-id="47855-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-213">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="47855-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47855-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-215">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47855-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="47855-216">**Nicht supportedqueries**</span><span class="sxs-lookup"><span data-stu-id="47855-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-217">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="47855-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="47855-218">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-219">Eine oder mehrere Abfragen, die den Satz von Klassen beschreiben, den der Klassen Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47855-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="47855-220">Verwenden Sie diese Eigenschaft, um den von **resultsetqueries** impliziten Satz von Klassen zu subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="47855-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="47855-221">**Version**</span><span class="sxs-lookup"><span data-stu-id="47855-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47855-222">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47855-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47855-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47855-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47855-224">Version dieses Klassen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="47855-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47855-225">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47855-225">Remarks</span></span>

<span data-ttu-id="47855-226">Die **\_ \_ classproviderregistration** -Klasse wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)abgeleitet, das von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="47855-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="47855-227">Die von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) geerbten Eigenschaften geben an, ob der Klassen Anbieter Datenabruf, Änderung, Löschung, Enumeration und Abfrage Verarbeitung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47855-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="47855-228">Die **interaktiontype** -Eigenschaft gibt an, ob der Klassen Anbieter als Pull-oder pushanbieter konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="47855-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="47855-229">Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="47855-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="47855-230">Die [**\_ \_ providerregistration**](--providerregistration.md) -Klasse definiert die [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="47855-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="47855-231">Nur Administratoren können einen Anbieter registrieren, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ classproviderregistration** erstellen.</span><span class="sxs-lookup"><span data-stu-id="47855-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="47855-232">Nur Administratoren können einen Anbieter löschen.</span><span class="sxs-lookup"><span data-stu-id="47855-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="47855-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47855-233">Requirements</span></span>



| <span data-ttu-id="47855-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47855-234">Requirement</span></span> | <span data-ttu-id="47855-235">Wert</span><span class="sxs-lookup"><span data-stu-id="47855-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="47855-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47855-236">Minimum supported client</span></span><br/> | <span data-ttu-id="47855-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47855-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="47855-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47855-238">Minimum supported server</span></span><br/> | <span data-ttu-id="47855-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47855-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="47855-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="47855-240">Namespace</span></span><br/>                | <span data-ttu-id="47855-241">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="47855-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="47855-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47855-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47855-243">**\_\_Objectproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="47855-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="47855-244">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="47855-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="47855-245">Registrieren eines Klassen Anbieters</span><span class="sxs-lookup"><span data-stu-id="47855-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="47855-246">Registrieren eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="47855-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="47855-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="47855-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

