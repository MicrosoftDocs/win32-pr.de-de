---
title: DVC-Plug-in-Registrierung
description: Beschreibt die Syntax für den DVC (Dynamic Virtual Channel)-Plug-in-Eintrag für den Remotedesktopverbindung-Client (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342152"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="c7dda-103">DVC-Plug-in-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c7dda-103">DVC plug-in registration</span></span>

<span data-ttu-id="c7dda-104">Das DVC-Plug-in (Dynamic Virtual Channel) ist für die Verwendung durch den Remotedesktopverbindung (RDC)-Client mithilfe einer der folgenden Methoden registriert:</span><span class="sxs-lookup"><span data-stu-id="c7dda-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="c7dda-105">Aufrufen der [**imstscadvancedsettings::p UT \_ plugindlls**](imstscadvancedsettings-plugindlls.md) -Methode des ActiveX-Steuer Elements Remotedesktopprotokoll (RDP).</span><span class="sxs-lookup"><span data-stu-id="c7dda-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="c7dda-106">Mehrere Einträge müssen durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="c7dda-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="c7dda-107">Der Plug-in-Eintrag wird an folgendem Speicherort in der Registrierung auf dem Computer geschrieben, auf dem der Remotedesktopverbindung-Client Prozess (RDC) gestartet wurde:</span><span class="sxs-lookup"><span data-stu-id="c7dda-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="c7dda-108">**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Standard** mäßige \\ **AddIns** Name eindeutiger \\ ***Plug-in-Name***</span><span class="sxs-lookup"><span data-stu-id="c7dda-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="c7dda-109">Sie müssen den eindeutigen Unterschlüssel für den *Plug-in-Namen* erstellen, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c7dda-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="c7dda-110">Der eindeutige Name des unter Schlüssels Name des *Plug-ins* ist eine beliebige Zeichenfolge, die das Plug-in identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="c7dda-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="c7dda-111">Die Zeichenfolge kann eine beliebige Kombination von Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="c7dda-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="c7dda-112">Unter dem *eindeutigen Plug-in-Namen* müssen Sie einen Eintrag hinzufügen, der das Plug-in identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7dda-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="c7dda-113">Name des Eintrags = **Name**</span><span class="sxs-lookup"><span data-stu-id="c7dda-113">Entry name = **Name**</span></span>

    <span data-ttu-id="c7dda-114">Datentyp = **reg \_ SZ** oder **reg \_ Expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="c7dda-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="c7dda-115">In beiden Fällen muss der Einstiegs Wert einem der folgenden Formate entsprechen:</span><span class="sxs-lookup"><span data-stu-id="c7dda-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="c7dda-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-in-einzllname*: {*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="c7dda-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="c7dda-117">Das Plug-in ist nicht notwendigerweise in der Windows-Registrierung als Component Object Model (com)-Objekt registriert, aber die dll wird als Prozess interner com-Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="c7dda-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="c7dda-118">Der RDC-Client lädt die durch *Plug-in-Name* angegebene DLL und ruft das COM-Objekt direkt mithilfe der *CLSID* ab.</span><span class="sxs-lookup"><span data-stu-id="c7dda-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="c7dda-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-in-einllname*"</span><span class="sxs-lookup"><span data-stu-id="c7dda-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="c7dda-120">Die dll implementiert die [**virtualchannelgetinstance**](virtualchannelgetinstance.md) -Funktion und exportiert Sie nach Namen.</span><span class="sxs-lookup"><span data-stu-id="c7dda-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="c7dda-121">Der RDC-Client verwendet die **virtualchannelgetinstance** -Funktion zum Abrufen von [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstellen Zeigern für alle Plug-ins, die von der dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7dda-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="c7dda-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="c7dda-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="c7dda-123">Der RDC-Client instanziiert das Plug-in als reguläres com-Objekt mithilfe von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="c7dda-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="c7dda-124">*Plug-* in: der vollständige Pfad und Dateiname der DLL-Datei.</span><span class="sxs-lookup"><span data-stu-id="c7dda-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="c7dda-125">Wenn der Datentyp **reg \_ Expand \_ SZ** ist, kann der Pfad nicht erweiterte Umgebungsvariablen enthalten, die zur Laufzeit erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="c7dda-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="c7dda-126">Wenn der Remotedesktopverbindung-Client (RDC) seine Initialisierung abgeschlossen hat, führt er für jedes registrierte Plug-in Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="c7dda-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="c7dda-127">Rufen Sie mithilfe einer der oben beschriebenen Methoden eine Instanz der [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle für jedes Plug-in ab.</span><span class="sxs-lookup"><span data-stu-id="c7dda-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="c7dda-128">Ruft die [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) -Methode für jede [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="c7dda-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="c7dda-129">Wenn der Client mehrmals eine [**Verbindung**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) mit dem gleichen oder mit einem anderen Server herstellt, gibt es möglicherweise mehrere Aufrufe der Verbindungs [**-und**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) Verbindungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="c7dda-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="c7dda-130">Der letzte-Befehl, den das Plug-in behandeln soll, wird [**beendet**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span><span class="sxs-lookup"><span data-stu-id="c7dda-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="c7dda-131">Es ist ein Signal, dass der RDC-Client (Remotedesktopverbindung) das Plug-in entladen soll.</span><span class="sxs-lookup"><span data-stu-id="c7dda-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 