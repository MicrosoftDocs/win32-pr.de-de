---
title: Interaktive Benutzeroberfläche
description: Der Anbieter, der das Authentifizierungsprotokoll implementiert, kann auch eine interaktive Benutzeroberfläche (UI) für das Protokoll bereitstellen.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f35ac3492e45e80721f800925a003edbb8116ac8c199a1b633e08a28de675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117780"
---
# <a name="interactive-user-interface"></a>Interaktive Benutzeroberfläche

Der Anbieter, der das Authentifizierungsprotokoll implementiert, kann auch eine interaktive Benutzeroberfläche (UI) für das Protokoll bereitstellen. Die interaktive Benutzeroberfläche ermöglicht dem Authentifizierungsprotokoll, während der Authentifizierungssitzung bei Bedarf zusätzliche Informationen vom Benutzer zu erhalten.

Die interaktive Benutzeroberfläche kann in derselben DLL wie das Authentifizierungsprotokoll oder in einer separaten DLL implementiert werden. Außerdem kann die DLL, die die interaktive Benutzeroberfläche implementiert, mehr als ein Authentifizierungsprotokoll unterstützen. Der Pfad zur DLL für die interaktive Benutzeroberfläche wird im [Registrierungswert RAS \_ EAP \_ VALUENAME \_ INTERACTIVEUI](authentication-protocol-registry-values.md) unter dem Schlüssel für das Authentifizierungsprotokoll gespeichert. Weitere Informationen zum Erstellen dieses Registrierungswerts finden Sie unter [EAP-Installation.](eap-installation.md)

Die DLL für die interaktive Benutzeroberfläche sollte Einstiegspunkte für die folgenden Funktionen exportieren:<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

Die interaktive Benutzeroberfläche muss [**WM \_ COMMAND-Meldungen**](../menurc/wm-command.md) unterstützen, bei [**denen LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) IDCANCEL entspricht.

Um die interaktive Benutzeroberfläche anzuzeigen, sollte das Authentifizierungsprotokoll das **fInvokeInteractiveUI-Mitglied** der [**STRUKTUR DER \_ OUTPUT-AUSGABE \_ VON OUTPUT von OUTPUT auf TRUE**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) **festlegen.** Das Authentifizierungsprotokoll kann optional auch die **Member pUIContextData** und **dwSizeOfUIContextData** auf **TRUE** festlegen. Der Authentifizierungsdienst verwendet die Werte dieser Member, um Kontextdaten an die interaktive Benutzeroberfläche zu übergeben. Das Authentifizierungsprotokoll gibt die **STRUKTUR FÜR DIE OUTPUT-Ausgabe VON OUTPUT \_ \_ als** Parameter in der [**RasEapMakeMessage-Funktion**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) zurück.

Der Authentifizierungsdienst ruft die interaktive Benutzeroberfläche auf, indem [**rasEapInvokeInteractiveUI aufgerufen wird.**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui) Der Dienst übergibt dann dem Authentifizierungsprotokoll einen Zeiger auf die Daten, die von der interaktiven Benutzeroberfläche beim nachfolgenden Aufruf von [**RasEapMakeMessage zurückgegeben werden.**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) Der Zeiger wird als Member [**einerBAU \_ EAP \_ INPUT-Struktur**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) übergeben. Nachdem **RasEapMakeMessage zurückgegeben** wurde, ruft der Dienst [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) auf, um den von den Informationen belegten Arbeitsspeicher frei zu geben. Daher sollte das Authentifizierungsprotokoll die Informationen während des Aufrufs von **RasEapMakeMessage** in einen privaten Speicherpuffer kopieren.

 

 