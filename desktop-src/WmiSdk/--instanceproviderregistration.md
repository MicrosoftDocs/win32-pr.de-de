---
description: Registriert Instanzanbieter in WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347706"
---
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="cd7d3-103">\_\_Instanceproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd7d3-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="cd7d3-104">Die **\_ \_ instanceproviderregistration** -System Klasse registriert Instanzanbieter in WMI.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="cd7d3-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cd7d3-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd7d3-107">Syntax</span></span>

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="cd7d3-108">Member</span><span class="sxs-lookup"><span data-stu-id="cd7d3-108">Members</span></span>

<span data-ttu-id="cd7d3-109">Die **\_ \_ instanceproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cd7d3-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="cd7d3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd7d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd7d3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd7d3-111">Properties</span></span>

<span data-ttu-id="cd7d3-112">Die **\_ \_ instanceproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd7d3-113">**Interaktionstyp**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-114">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-116">Gibt an, dass ein Klassen-oder Instanzanbieter Daten bereitstellt, oder ruft Daten aus WMI und dem Common Information Model (CIM)-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="cd7d3-117">Pull-Anbieter unterstützen den dynamischen Zugriff auf Ihre Daten. und pushanbieter speichern Ihre Daten im CIM-Repository und verwenden WMI, um den Zugriff darauf zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="cd7d3-118">Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="cd7d3-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="cd7d3-119">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cd7d3-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="cd7d3-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="cd7d3-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-121">Der Anbieter ist ein Pull-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="cd7d3-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="cd7d3-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-123">Der Anbieter ist ein Push-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="cd7d3-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Pushverify** (2)</span><span class="sxs-lookup"><span data-stu-id="cd7d3-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-125">Der Anbieter ist ein Push-Verify-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="cd7d3-126">Beachten Sie, dass Push-Verify-Anbieter derzeit nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd7d3-127">**ab**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-128">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd7d3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-130">Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad zum Instanzanbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="cd7d3-131">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd7d3-132">**Querysupportlevels**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cd7d3-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-135">Array der Typen der Anbieter bezogenen Unterstützung für die Abfrage Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="cd7d3-136">Klassen Anbieter unterstützen nicht alle Abfrage Typen.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="cd7d3-137">Instanzanbieter können **querysupportlevels** auf **null** festlegen, wenn Sie die Abfrage Verarbeitung nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="cd7d3-138">Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode, und legen Sie diese Eigenschaft auf einen oder mehrere der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="cd7d3-139">("WQL: unaryselect")</span><span class="sxs-lookup"><span data-stu-id="cd7d3-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd7d3-140">("WQL: Verweise")</span><span class="sxs-lookup"><span data-stu-id="cd7d3-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd7d3-141">("WQL: assoziatoren")</span><span class="sxs-lookup"><span data-stu-id="cd7d3-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd7d3-142">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="cd7d3-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd7d3-143">**Supportsbatching**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-146">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd7d3-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-150">**True** gibt an, dass der Anbieter das Löschen von Daten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="cd7d3-151">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd7d3-151">True</span></span>
</dt> <dd>

<span data-ttu-id="cd7d3-152">Der Anbieter unterstützt das Löschen von Klassen oder Instanzen durch Implementieren von [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassen Anbieter) oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter).</span><span class="sxs-lookup"><span data-stu-id="cd7d3-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="cd7d3-153">False</span><span class="sxs-lookup"><span data-stu-id="cd7d3-153">False</span></span>
</dt> <dd>

<span data-ttu-id="cd7d3-154">Der Anbieter unterstützt keine Daten Löschung und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) oder [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd7d3-155">**Supportsenumeration**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-156">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-158">**True** gibt an, dass der Anbieter datenenumeration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="cd7d3-159">Fall</span><span class="sxs-lookup"><span data-stu-id="cd7d3-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-160">Der Anbieter unterstützt die datenenumeration durch Implementieren eines der beiden Typen [**IWbemServices:: | ateclassenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (Klassen Anbieter) oder [**IWbemServices:: feateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (Instanzanbieter).</span><span class="sxs-lookup"><span data-stu-id="cd7d3-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="cd7d3-161">Alarm</span><span class="sxs-lookup"><span data-stu-id="cd7d3-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-162">Der Anbieter unterstützt keine datenenumeration und gibt [](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)den **WBEM \_ E- \_ Anbieter \_ \_** zurück, [**der**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) nicht in der Lage ist, von "" aus "", "", "", "", "", ""</span><span class="sxs-lookup"><span data-stu-id="cd7d3-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd7d3-163">**Supportsget**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-164">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-166">**True** gibt an, dass der Klassen-oder Instanzanbieter den Datenabruf unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="cd7d3-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="cd7d3-167">True</span></span>
</dt> <dd>

<span data-ttu-id="cd7d3-168">Der Anbieter unterstützt den Datenabruf durch Implementieren von [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="cd7d3-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="cd7d3-169">False</span><span class="sxs-lookup"><span data-stu-id="cd7d3-169">False</span></span>
</dt> <dd>

<span data-ttu-id="cd7d3-170">Der Anbieter unterstützt nicht das Abrufen von Daten und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd7d3-171">**Supportsput**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-174">**True** gibt an, dass der Klassen-oder Instanzanbieter die Datenänderung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="cd7d3-175">Fall</span><span class="sxs-lookup"><span data-stu-id="cd7d3-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-176">Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren einer der folgenden Methoden: [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter).</span><span class="sxs-lookup"><span data-stu-id="cd7d3-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="cd7d3-177">Alarm</span><span class="sxs-lookup"><span data-stu-id="cd7d3-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="cd7d3-178">Der Anbieter unterstützt keine Datenänderungen und gibt den **WBEM E-Anbieter zurück, der \_ nicht \_ \_ \_** von [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) oder [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd7d3-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd7d3-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd7d3-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cd7d3-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd7d3-182">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd7d3-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd7d3-183">Remarks</span></span>

<span data-ttu-id="cd7d3-184">Die **\_ \_ instanceproviderregistration** -Klasse wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)abgeleitet, das von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="cd7d3-185">Nur Administratoren können einen Instanzanbieter registrieren, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ instanceproviderregistration** erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="cd7d3-186">Nur Administratoren können einen Anbieter löschen.</span><span class="sxs-lookup"><span data-stu-id="cd7d3-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7d3-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd7d3-187">Requirements</span></span>



| <span data-ttu-id="cd7d3-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd7d3-188">Requirement</span></span> | <span data-ttu-id="cd7d3-189">Wert</span><span class="sxs-lookup"><span data-stu-id="cd7d3-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cd7d3-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd7d3-190">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7d3-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd7d3-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cd7d3-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd7d3-192">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7d3-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd7d3-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cd7d3-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd7d3-194">Namespace</span></span><br/>                | <span data-ttu-id="cd7d3-195">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="cd7d3-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cd7d3-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd7d3-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7d3-197">**\_\_Objectproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="cd7d3-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="cd7d3-198">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="cd7d3-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="cd7d3-199">Registrieren eines Klassen Anbieters</span><span class="sxs-lookup"><span data-stu-id="cd7d3-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="cd7d3-200">Registrieren eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="cd7d3-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

