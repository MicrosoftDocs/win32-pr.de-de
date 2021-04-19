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
# <a name="dvc-plug-in-registration"></a>DVC-Plug-in-Registrierung

Das DVC-Plug-in (Dynamic Virtual Channel) ist für die Verwendung durch den Remotedesktopverbindung (RDC)-Client mithilfe einer der folgenden Methoden registriert:

-   Aufrufen der [**imstscadvancedsettings::p UT \_ plugindlls**](imstscadvancedsettings-plugindlls.md) -Methode des ActiveX-Steuer Elements Remotedesktopprotokoll (RDP). Mehrere Einträge müssen durch Kommas getrennt werden.
-   Der Plug-in-Eintrag wird an folgendem Speicherort in der Registrierung auf dem Computer geschrieben, auf dem der Remotedesktopverbindung-Client Prozess (RDC) gestartet wurde:

    **HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Standard** mäßige \\ **AddIns** Name eindeutiger \\ ***Plug-in-Name***

    > [!Note]  
    > Sie müssen den eindeutigen Unterschlüssel für den *Plug-in-Namen* erstellen, wenn er nicht vorhanden ist. Der eindeutige Name des unter Schlüssels Name des *Plug-ins* ist eine beliebige Zeichenfolge, die das Plug-in identifizieren kann. Die Zeichenfolge kann eine beliebige Kombination von Zeichen sein.

     

    Unter dem *eindeutigen Plug-in-Namen* müssen Sie einen Eintrag hinzufügen, der das Plug-in identifiziert.

    Name des Eintrags = **Name**

    Datentyp = **reg \_ SZ** oder **reg \_ Expand \_ SZ**

In beiden Fällen muss der Einstiegs Wert einem der folgenden Formate entsprechen:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-in-einzllname*: {*CLSID*}"
</dt> <dd>

Das Plug-in ist nicht notwendigerweise in der Windows-Registrierung als Component Object Model (com)-Objekt registriert, aber die dll wird als Prozess interner com-Objekt implementiert. Der RDC-Client lädt die durch *Plug-in-Name* angegebene DLL und ruft das COM-Objekt direkt mithilfe der *CLSID* ab.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-in-einllname*"
</dt> <dd>

Die dll implementiert die [**virtualchannelgetinstance**](virtualchannelgetinstance.md) -Funktion und exportiert Sie nach Namen. Der RDC-Client verwendet die **virtualchannelgetinstance** -Funktion zum Abrufen von [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstellen Zeigern für alle Plug-ins, die von der dll implementiert werden.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

Der RDC-Client instanziiert das Plug-in als reguläres com-Objekt mithilfe von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der *CLSID*.

</dd> </dl>

> [!Note]  
> *Plug-* in: der vollständige Pfad und Dateiname der DLL-Datei. Wenn der Datentyp **reg \_ Expand \_ SZ** ist, kann der Pfad nicht erweiterte Umgebungsvariablen enthalten, die zur Laufzeit erweitert werden.

 

Wenn der Remotedesktopverbindung-Client (RDC) seine Initialisierung abgeschlossen hat, führt er für jedes registrierte Plug-in Folgendes aus:

1.  Rufen Sie mithilfe einer der oben beschriebenen Methoden eine Instanz der [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle für jedes Plug-in ab.
2.  Ruft die [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) -Methode für jede [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle auf.
3.  Wenn der Client mehrmals eine [**Verbindung**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) mit dem gleichen oder mit einem anderen Server herstellt, gibt es möglicherweise mehrere Aufrufe der Verbindungs [**-und**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) Verbindungsmethoden.
4.  Der letzte-Befehl, den das Plug-in behandeln soll, wird [**beendet**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated). Es ist ein Signal, dass der RDC-Client (Remotedesktopverbindung) das Plug-in entladen soll.

 

 