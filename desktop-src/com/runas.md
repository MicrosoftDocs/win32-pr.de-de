---
title: RunAs
description: Konfiguriert eine Klasse so, dass Sie unter einem bestimmten Benutzerkonto ausgeführt wird, wenn Sie von einem Remote Client aktiviert wird, ohne als Dienst Anwendung geschrieben zu werden.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Runas-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337262"
---
# <a name="runas"></a>RunAs

Konfiguriert eine Klasse so, dass Sie unter einem bestimmten Benutzerkonto ausgeführt wird, wenn Sie von einem Remote Client aktiviert wird, ohne als Dienst Anwendung geschrieben zu werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>Bemerkungen

Der-Wert gibt den Benutzernamen an und muss entweder die Form *username*, den *Domänen ***\\*** Benutzer* Namen oder die Zeichenfolge "Interactive User" aufweisen. Sie können auch die Zeichen folgen "NT Authority \\ LocalService" (für lokaler Dienst) und "NT Authority \\ Network Service" (für Netzwerkdienst) angeben. Sie können auch die Zeichenfolge "NT Authority \\ System" angeben, wenn "{*AppID \_ GUID*}" auf einen com-Server verweist, der bereits gestartet wurde oder über einen Eintrag in der Klassen Tabelle verfügt. Allerdings können Sie "NT Authority \\ System" nicht mit einem com-Server verwenden, der noch nicht gestartet wurde. Das Standard Kennwort für "NT Authority \\ LocalService", "NT Authority \\ Network Service" und "NT Authority \\ System" ist "" (leere Zeichenfolge).

> [!Note]  
> Ab Windows Vista ist ein leeres Kennwort nicht mehr erforderlich, um die \\ runas-Einstellungen "NT Authority LocalService", "NT Authority \\ Network Service" und "NT Authority \\ System"  zu konfigurieren.

 

Klassen, die so konfiguriert sind, dass Sie als ein bestimmter Benutzer ausgeführt werden, sind möglicherweise nicht unter einer anderen Identität registriert, sodass Aufrufe von [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) mit dieser CLSID fehlschlagen, es sei denn, der Prozess wurde von com im Auftrag einer tatsächlichen Aktivierungs Anforderung gestartet.

Der Benutzername wird aus dem **runas** -Wert unter dem **AppID** -Schlüssel der Klasse entnommen. Wenn der Benutzername "interaktiver Benutzer" ist, wird der Server in der Identität des aktuell angemeldeten Benutzers ausgeführt und mit dem interaktiven Desktop verbunden.

Andernfalls wird das Kennwort aus einem Teil der Registrierung abgerufen, der nur für Administratoren des Computers und für das System verfügbar ist. Der Benutzername und das Kennwort werden dann verwendet, um eine Anmelde Sitzung zu erstellen, in der der Server ausgeführt wird. Wenn der Benutzer auf diese Weise gestartet wird, wird er mit einer eigenen Desktop-und Fenster Station ausgeführt, und es werden keine Fenster Handles, die Zwischenablage oder andere Elemente der Benutzeroberfläche mit dem interaktiven Benutzer oder anderen Benutzern, die in anderen Benutzerkonten ausgeführt werden, gemeinsam verwendet.

Zum Festlegen eines Kennworts für eine **runas** -Klasse müssen Sie das im System Verzeichnis installierte Verwaltungs Tool DCOMCNFG verwenden.

Bei von DCOM-Servern verwendeten **runas** -Identitäten muss das in dem Wert angegebene Benutzerkonto über die Berechtigung zum Anmelden als Batch Auftrag verfügen. Dieses Recht kann mithilfe des Verwaltungs Tools für lokale Sicherheitsrichtlinien hinzugefügt werden. Wechseln Sie zu **lokale Richtlinien** , und öffnen Sie **Zuweisung von Benutzerrechten**. Wählen Sie **als Batch Auftrag anmelden aus**, und fügen Sie das Benutzerkonto hinzu.

Der **runas** -Wert wird nicht für Server verwendet, die für die Ausführung als Dienste konfiguriert sind. COM-Dienste, die unter einer anderen Identität als "LocalSystem" ausgeführt werden müssen, müssen den entsprechenden Benutzernamen und das Kennwort mithilfe des System Steuerungs Applets der Dienste oder der Dienst Controller Funktionen festlegen. (Weitere Informationen zu diesen Funktionen finden Sie unter [Dienste](/windows/desktop/Services/services).)

> [!Note]  
> Ab Microsoft Windows Server 2003 wird die AppID der Klasse explizit aus den **HKEY- \_ \_ Software Klassen der lokalen Computer- \\ \\ \\ AppID** gelesen, die im Gegensatz zu den meisten Registrierungs Schlüsseln nicht mit der Stamm- **\_ \_ \\ AppID der HKEY-Klassen** austauschbar ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> </dl>

 

 