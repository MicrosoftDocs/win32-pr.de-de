---
description: Die Skript-API für WMI enthält Flags, allgemeine Werte und Fehlercodes.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Skript-API-Konstanten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347894"
---
# <a name="scripting-api-constants"></a><span data-ttu-id="1884e-103">Skript-API-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1884e-103">Scripting API Constants</span></span>

<span data-ttu-id="1884e-104">WMI verwendet verschiedene Typen von Konstanten im *IFlags* -Parameter von Methoden aufrufen in der [Skript-API für WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1884e-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="1884e-105">Visual Basic Anwendungen können die Typbibliothek für die Skript-API, wbemdisp. tlb, enthalten.</span><span class="sxs-lookup"><span data-stu-id="1884e-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="1884e-106">Skripts können nicht auf Konstanten in der Typbibliothek zugreifen, es sei denn, Sie verwenden die <REFERENCE> <OBJECT> Tags oder aus dem XML-Dateiformat von Windows Script Host (WSH), wie in [Verwenden der WMI-Skriptingtypbibliothek](using-the-wmi-scripting-type-library.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1884e-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="1884e-107">Andernfalls muss ein Skript den Wert der Konstanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="1884e-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="1884e-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1884e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1884e-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**Wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-110">Definieren Sie die Sicherheits Authentifizierungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="1884e-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**Wbemchangeflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-112">Definieren Sie, wie ein Schreibvorgang für eine Klasse oder eine Instanz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1884e-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**Wbemcimtypeerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-114">Definieren Sie die gültigen CIM-Typen eines Eigenschafts Werts.</span><span class="sxs-lookup"><span data-stu-id="1884e-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**Wbemcomparisonflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-116">Definieren Sie die Einstellungen für den Objektvergleich und werden von der Datei " [**errbemubject. CompareTo \_**](swbemobject-compareto-.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1884e-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="1884e-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**Wbemconnectoptionsenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-118">Definiert ein sicherheitsflag, das in Aufrufen der Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " als Parameter verwendet wird, wenn eine Verbindung mit WMI auf einem Remote Computer fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1884e-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-120">Hiermit werden die Fehler definiert, die von der [Skript-API für WMI](scripting-api-for-wmi.md) -Aufrufe zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="1884e-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**Wbemflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-122">Definiert Konstanten, die von [**SWbemServices.Execquery**](swbemservices-execquery.md)verwendet werden [**,SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md), [**Swap Services. SubclassesOf**](swbemservices-subclassesof.md)und [**Swap Services. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="1884e-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="1884e-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**Wbemimpersonationlevelenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-124">Definieren Sie die Sicherheits Identitätswechsel Ebenen.</span><span class="sxs-lookup"><span data-stu-id="1884e-124">Define the security impersonation levels.</span></span> <span data-ttu-id="1884e-125">Diese Konstanten werden mit " [**Swap Security**](swbemsecurity.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1884e-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="1884e-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**Wbemubjecttextformataufumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-127">Hiermit werden die gültigen Objekt Textformate definiert, die von " [**errbemubjectex. \_ gettext**](swbemobjectex-gettext-.md)" verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1884e-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="1884e-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-129">Definieren von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="1884e-129">Define privileges.</span></span> <span data-ttu-id="1884e-130">Diese Konstanten werden mit " [**Swap Security**](swbemsecurity.md) " verwendet, um die Berechtigungen zu erteilen, die für einige Vorgänge erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1884e-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**Wbemqueryflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-132">Definieren Sie die Tiefe der Enumeration oder der Abfrage, die bestimmt, wie viele Objekte von einem-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1884e-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**Wbemtextflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="1884e-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-134">Definiert den Inhalt des generierten Objekt Texts und wird von " [**errbemubject. getobjecttext \_**](swbemobject-getobjecttext-.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1884e-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="1884e-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**Wbemtimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="1884e-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="1884e-136">Definiert die Timeout Konstanten.</span><span class="sxs-lookup"><span data-stu-id="1884e-136">Defines the time-out constants.</span></span> <span data-ttu-id="1884e-137">Diese Konstante wird von " [**errbemeventsource. NextEvent**](swbemeventsource-nextevent.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1884e-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="1884e-138">Kombinieren von Flags</span><span class="sxs-lookup"><span data-stu-id="1884e-138">Combining Flags</span></span>

<span data-ttu-id="1884e-139">Sie können Flags kombinieren, um mehr als einen Aspekt des API-Aufrufes zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="1884e-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="1884e-140">Um z. b. einen [*semisynchronen*](gloss-s.md) -Befehl zu erstellen, muss der *IFlags* -Parameter in einem [**SWbemServices.Exe\_ cquery**](swbemservices-execquery.md) -Befehl zwei Flags enthalten: **wbemFlagReturnImmediately** und **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="1884e-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="1884e-141">Der Wert von **wbemFlagReturnImmediately** ist 16, und der Wert von **wbemFlagForwardOnly** ist 32.</span><span class="sxs-lookup"><span data-stu-id="1884e-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="1884e-142">Da auf die Konstanten nicht über den Namen zugegriffen werden kann, werden die Werte dieser Flags kombiniert, sodass ein *IFlags* -Wert von 48 erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="1884e-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="1884e-143">Das folgende Skript Beispiel zeigt den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="1884e-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="1884e-144">Nicht alle Flags können kombiniert werden, da sich viele gegenseitig ausschließen und zu unvorhersehbaren Ergebnissen führen können.</span><span class="sxs-lookup"><span data-stu-id="1884e-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1884e-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1884e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1884e-146">Skript-API für WMI</span><span class="sxs-lookup"><span data-stu-id="1884e-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



