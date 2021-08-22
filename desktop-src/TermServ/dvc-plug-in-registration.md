---
title: DVC-Plug-In-Registrierung
description: Beschreibt die Syntax für den DVC-Plug-In-Eintrag (Dynamischer virtueller Kanal) für den rdc-Client (Remotedesktopverbindung).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d3660b4d9c704c9a59335cede886085f13414991dc2dc913185d407e0a3c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515527"
---
# <a name="dvc-plug-in-registration"></a>DVC-Plug-In-Registrierung

Das DVC-Plug-In (Dynamischer virtueller Kanal) wird für die Verwendung durch den rdc-Client (Remotedesktopverbindung) mit einer der folgenden Methoden registriert:

-   Aufrufen der [**IMsTscAdvancedSettings::p ut \_ PluginDlls-Methode**](imstscadvancedsettings-plugindlls.md) des Remotedesktopprotokoll (RDP) ActiveX-Steuerelements. Mehrere Einträge müssen durch Kommas getrennt werden.
-   Schreiben des Plug-In-Eintrags an den folgenden Speicherort in der Registrierung auf dem Computer, auf dem der Remotedesktopverbindung-Clientprozess gestartet wird:

    **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Default** \\ **AddIns** \\ **_unique plug-in name_**

    > [!Note]  
    > Sie müssen den Unterschlüssel für den *eindeutigen Plug-In-Namen* erstellen, wenn er nicht vorhanden ist. Der *eindeutige Unterschlüsselname des Plug-Ins* ist eine beliebige Zeichenfolge, die das Plug-In identifizieren kann. Die Zeichenfolge kann eine beliebige Kombination von Zeichen sein.

     

    Unter *dem eindeutigen Plug-In-Namen* müssen Sie einen Eintrag hinzufügen, der das Plug-In identifiziert.

    Eintragsname = **Name**

    Datentyp = **REG \_ SZ** oder **REG EXPAND \_ \_ SZ**

In beiden Fällen muss der Eintragswert einem der folgenden Formate entsprechen:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-InDLLName*:{*CLSID*}"
</dt> <dd>

Das Plug-In ist nicht unbedingt in der Windows-Registrierung als COM-Objekt (Component Object Model) registriert, aber die DLL wird als PROZESS-COM-Objekt implementiert. Der RDC-Client lädt die durch *Plug-InDLLName* angegebene DLL und ruft das COM-Objekt direkt mithilfe von *CLSID* ab.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-InDLLName*"
</dt> <dd>

Die DLL implementiert die [**VirtualChannelGetInstance-Funktion**](virtualchannelgetinstance.md) und exportiert sie nach Namen. Der RDC-Client verwendet die **VirtualChannelGetInstance-Funktion,** um [**IWTSPlugin-Schnittstellenzeiger**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) für alle Plug-Ins abzurufen, die von der DLL implementiert werden.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

Der RDC-Client instanziiert das Plug-In mithilfe von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der *CLSID* als reguläres COM-Objekt.

</dd> </dl>

> [!Note]  
> *Plug-InDLLName* stellt den vollständigen Pfad und Dateinamen der .dll Datei dar. Wenn der Datentyp **REG \_ EXPAND \_ SZ** ist, kann der Pfad nicht erweiterte Umgebungsvariablen enthalten, die zur Laufzeit erweitert werden.

 

Wenn der Remotedesktopverbindung-Client (RDC) seine Initialisierung beendet, führt er für jedes registrierte Plug-In Folgendes aus:

1.  Rufen Sie mithilfe einer der oben beschriebenen Methoden eine Instanz der [**IWTSPlugin-Schnittstelle**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) für jedes Plug-In ab.
2.  Rufen Sie die [**Initialize-Methode**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) jeder [**IWTSPlugin-Schnittstelle**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) auf.
3.  Wenn der Client mehrmals eine Verbindung mit demselben oder einem anderen Server herstellt, kann es mehrere Aufrufe der Methoden [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) und [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) geben.
4.  Der letzte Aufruf, den das Plug-In verarbeiten soll, ist [**Beendet.**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated) Es ist ein Signal, dass der rdc-Client (Remotedesktopverbindung) das Plug-In entladen wird.

 

 