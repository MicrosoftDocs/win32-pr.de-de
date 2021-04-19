---
description: Standardmäßig empfängt eine Anwendung oder ein Skript Daten vom entsprechenden Anbieter, wenn zwei Versionen von Anbietern vorhanden sind.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Anfordern von WMI-Daten auf einer 64-Bit-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356877"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="f2315-103">Anfordern von WMI-Daten auf einer 64-Bit-Plattform</span><span class="sxs-lookup"><span data-stu-id="f2315-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="f2315-104">Standardmäßig empfängt eine Anwendung oder ein Skript Daten vom entsprechenden Anbieter, wenn zwei Versionen von Anbietern vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f2315-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="f2315-105">Der 32-Bit-Anbieter gibt Daten an eine 32-Bit-Anwendung zurück, einschließlich aller Skripts, und der 64-Bit-Anbieter gibt Daten an die von 64 Bit kompilierten Anwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="f2315-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="f2315-106">Allerdings kann eine Anwendung oder ein Skript Daten vom nicht standardmäßigen Anbieter anfordern, wenn dies der Fall ist, indem WMI über Flags für Methodenaufrufe benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="f2315-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="f2315-107">Kontextflags</span><span class="sxs-lookup"><span data-stu-id="f2315-107">Context Flags</span></span>

<span data-ttu-id="f2315-108">Die zeichenfolgenflags **\_ \_ providerarchitecture** und Requirements **\_ \_ darchitecture** verfügen über eine Reihe von Werten, die von WMI verarbeitet, jedoch nicht in SDK-Header-oder Typbibliotheks Dateien definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f2315-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="f2315-109">Die Werte werden in einen Kontext Parameter eingefügt, um WMI zu signalisieren, dass Daten vom nicht standardmäßigen Anbieter angefordert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2315-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="f2315-110">Im folgenden werden die Flags und die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2315-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="f2315-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_Providerarchitecture**</span><span class="sxs-lookup"><span data-stu-id="f2315-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="f2315-112">Ganzzahliger Wert, entweder 32 oder 64, der die 32-Bit-oder 64-Bit-Version angibt.</span><span class="sxs-lookup"><span data-stu-id="f2315-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="f2315-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_Requirements darchitecture**</span><span class="sxs-lookup"><span data-stu-id="f2315-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="f2315-114">Boolescher Wert, der zusätzlich zu **\_ \_ providerarchitecture** verwendet wird, um das Laden der angegebenen Anbieter Version zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="f2315-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="f2315-115">Wenn die Version nicht verfügbar ist, gibt WMI den Fehler 0x80041013, **wbemErrProviderLoadFailure** für die Visual Basic und den **\_ \_ \_ Lade \_ Fehler des WBEM E-Anbieters** für C++ zurück.</span><span class="sxs-lookup"><span data-stu-id="f2315-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="f2315-116">Der Standardwert für dieses Flag, wenn es nicht angegeben ist, ist **false**.</span><span class="sxs-lookup"><span data-stu-id="f2315-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="f2315-117">Auf einem 64-Bit-System, das über parallele Versionen eines Anbieters verfügt, empfängt eine 32-Bit-Anwendung oder ein-Skript automatisch Daten vom 32-Bit-Anbieter, es sei denn, diese Flags werden bereitgestellt und geben an, dass die 64-Bit-Anbieter Daten zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2315-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="f2315-118">Verwenden der kontextflags</span><span class="sxs-lookup"><span data-stu-id="f2315-118">Using the Context Flags</span></span>

<span data-ttu-id="f2315-119">C++-Anwendungen können die [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Schnittstelle mit [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) verwenden, um die Verwendung eines nicht standardmäßigen Anbieters mit WMI zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f2315-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="f2315-120">Bei der Skripterstellung und Visual Basic müssen Sie ein Objekt vom Typ "WS- [**namedvalueset**](swbemnamedvalueset.md) " erstellen, das die Flags für den *objwbemnamedvalueset* -Parameter von [**SWbemServices.Execmethod**](swbemservices-execmethod.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="f2315-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="f2315-121">Weitere Informationen zum Einrichten der Parameter Objekte für diesen Befehl finden Sie unter [Erstellen von inparameter-Objekten und Auswerten von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f2315-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="f2315-122">Sie können Skripts und Anwendungen auf sichere Weise mithilfe der kontextflags in älteren Betriebssystemen ausführen, da Sie von WMI in Systemen ignoriert werden, in denen Sie nicht implementiert sind.</span><span class="sxs-lookup"><span data-stu-id="f2315-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="f2315-123">Während 32-Bit-und 64-Bit-Versionen des System Registrierungs Anbieters vorhanden sind, beachten Sie, dass nur eine Version des WMI-Repository vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f2315-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="f2315-124">Zugreifen auf die standardmäßige Registrierungs Struktur</span><span class="sxs-lookup"><span data-stu-id="f2315-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="f2315-125">In der folgenden Reihe von Beispielen wird der [Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider)verwendet, bei dem auf 64-Bit-Betriebssystemen nebeneinander 32-Bit-und 64-Bit-Versionen vorinstalliert sind.</span><span class="sxs-lookup"><span data-stu-id="f2315-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="f2315-126">In diesen Beispielen erhalten 32-Bit-Clients vom Anbieter zurückgegebene Daten vom 32-Bit-Knoten **HKEY \_ local \_ Machine \\ Software \\ Wow6432Node \\ Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="f2315-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="f2315-127">64-Bit-Clients erhalten vom Anbieter zurückgegebene Daten vom 64-Bit-Knoten **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Logging**.</span><span class="sxs-lookup"><span data-stu-id="f2315-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="f2315-128">Die Skripts veranschaulichen, wie Sie die Methoden der Klasse [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) der Registrierung über [**SWbemServices.Execmethod**](swbemservices-execmethod.md) zum Abrufen von Daten aus der 32-Bit-Registrierungs Struktur abrufen.</span><span class="sxs-lookup"><span data-stu-id="f2315-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="f2315-129">Das folgende Skript ruft Daten vom Anbieter ab, die mit der Bitbreite des Aufrufers übereinstimmen (in diesem Fall 64 Bits), da es sich um ein Skript handelt, das unter dem 64-Bit Windows Script Host (WSH) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2315-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="f2315-130">Das Skript ruft den Wert aus dem 64-Bit-Registrierungs Knoten **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM \\ Logging** anstelle des 32-Bit-Knotens **HKEY \_ local \_ Machine \\ Software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM** ab.</span><span class="sxs-lookup"><span data-stu-id="f2315-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



<span data-ttu-id="f2315-131">Wenn der **Protokollierungs** Wert in der standardhive auf 1 festgelegt ist, sollte die Ausgabe des Skripts in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="f2315-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="f2315-132">Beispiel: Anfordern der 32-Bit-Registrierungs Struktur auf einem 64-Bit-Computer</span><span class="sxs-lookup"><span data-stu-id="f2315-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="f2315-133">Im folgenden geänderten Beispiel des Standard Skripts wird das Flag für die **\_ \_ providerarchitecture** -Zeichenfolge verwendet, um Zugriff auf die 32-Bit-Registrierungsdaten auf einem 64-Bit-Computer anzufordern.</span><span class="sxs-lookup"><span data-stu-id="f2315-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="f2315-134">Der Aufrufer ist mit der 32-Bit-Struktur verbunden, unabhängig davon, ob es sich um eine 32-oder 64-Bit-Anwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="f2315-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="f2315-135">Beispiel: Erzwingen von WMI für den Zugriff auf die 32-Bit-Registrierungs Struktur auf einem 64-Bit-Computer</span><span class="sxs-lookup"><span data-stu-id="f2315-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="f2315-136">Durch die folgende Änderung des obigen Skripts durch Hinzufügen der Flags **\_ \_ providerarchitecture** und Requirements **\_ \_ darchitecture** zum Kontext Parameter wird WMI gezwungen, den 32-Bit-Anbieter zu laden und 32-Bit-Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f2315-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="f2315-137">Wenn der Anbieter nicht vorhanden ist, tritt ein Fehler beim Laden des Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="f2315-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="f2315-138">Das Kontext Objekt muss bei der Verbindung mit WMI durch Aufrufen von "WS- [**Locator. ConnectServer**](swbemlocator-connectserver.md)" bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2315-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a><span data-ttu-id="f2315-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2315-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2315-140">Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer</span><span class="sxs-lookup"><span data-stu-id="f2315-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
