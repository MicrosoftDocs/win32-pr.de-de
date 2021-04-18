---
title: Interaktive Benutzeroberfläche
description: Der Hersteller, der das Authentifizierungsprotokoll implementiert, kann auch eine interaktive Benutzeroberfläche (User Interface, UI) für das Protokoll bereitstellen.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761799969f4e439a65534ab551f09b3788e95ba7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339054"
---
# <a name="interactive-user-interface"></a>Interaktive Benutzeroberfläche

Der Hersteller, der das Authentifizierungsprotokoll implementiert, kann auch eine interaktive Benutzeroberfläche (User Interface, UI) für das Protokoll bereitstellen. Die interaktive Benutzeroberfläche ermöglicht es dem Authentifizierungsprotokoll, im Verlauf der Authentifizierungs Sitzung zusätzliche Informationen vom Benutzer zu erhalten.

Die interaktive Benutzeroberfläche kann in derselben DLL wie das Authentifizierungsprotokoll oder in einer separaten dll implementiert werden. Außerdem kann die dll, die die interaktive Benutzeroberfläche implementiert, mehr als ein Authentifizierungsprotokoll unterstützen. Der Pfad zur DLL für die interaktive Benutzeroberfläche wird im RAS-Registrierungs Wert " [ \_ EAP \_ valueName \_ interactiveui](authentication-protocol-registry-values.md) " unter dem Schlüssel für das Authentifizierungsprotokoll gespeichert. Weitere Informationen zum Erstellen dieses Registrierungs Werts finden Sie unter [EAP-Installation](eap-installation.md).

Die DLL für die interaktive Benutzeroberfläche sollte Einstiegspunkte für die folgenden Funktionen exportieren:<dl>

[**Raseapinvokeinteractiveui**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**Raseapfrememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

Die interaktive Benutzeroberfläche muss [**WM- \_ Befehls**](../menurc/wm-command.md) Nachrichten unterstützen, bei denen [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) gleich IDCANCEL ist.

Um die interaktive Benutzeroberfläche anzuzeigen, sollte das Authentifizierungsprotokoll den **finvokeinteractiveui** -Member der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Struktur auf " **true**" festlegen. Mit dem Authentifizierungsprotokoll können optional auch die Member **puicontextdata** und **dwsizeofuicontextdata** auf **true** festgelegt werden. Der Authentifizierungsdienst verwendet die Werte dieser Member, um Kontext Daten an die interaktive Benutzeroberfläche zu übergeben. Das Authentifizierungsprotokoll gibt die **PPP- \_ EAP- \_ Ausgabe** Struktur als Parameter in der [**raseapmakemesage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) -Funktion zurück.

Der Authentifizierungsdienst Ruft die interaktive Benutzeroberfläche durch Aufrufen von [**raseapinvokeinteractiveui**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)auf. Anschließend übergibt der Dienst dem Authentifizierungsprotokoll einen Zeiger auf die Daten, die von der interaktiven Benutzeroberfläche im anschließenden Aufrufer von [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))zurückgegeben werden. Der Zeiger wird als Member einer [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur übermittelt. Nachdem **raseapmakemess** zurückgegeben wurde, ruft der Dienst [**raseapfreememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) auf, um den von den Informationen belegten Arbeitsspeicher freizugeben. Daher sollte das Authentifizierungsprotokoll die Informationen während des Aufrufens von **raseapmakemess** in einen privaten Speicherpuffer kopieren.

 

 