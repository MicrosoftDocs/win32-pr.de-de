---
description: Um die Sicherheit des Host Prozesses (wmiprvse.exe) des freigegebenen Anbieters des Windows-Verwaltungsinstrumentation (WMI) zu verbessern, wurden Änderungen an Windows-Plattformen vorgenommen, mit denen der Anbieter Host Prozess mit einer Dienst Sicherheits-ID (SID) gesichert wird.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Registrierungsschlüssel und-Werte zum Steuern der Anbieter Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350934"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Registrierungsschlüssel und-Werte zum Steuern der Anbieter Sicherheit

Um die Sicherheit des Host Prozesses (wmiprvse.exe) des freigegebenen Anbieters des Windows-Verwaltungsinstrumentation (WMI) zu verbessern, wurden Änderungen an Windows-Plattformen vorgenommen, mit denen der Anbieter Host Prozess mit einer [*Dienst Sicherheits-ID (SID)*](gloss-s.md)gesichert wird. Durch diese Änderungen werden die folgenden Betriebsmodi für den freigegebenen WMI-Host eingeführt: sicher und kompatibel.

Die folgenden Abschnitte werden in diesem Thema behandelt:

-   [Sicherer und kompatibler Modus](#secure-and-compatible-modes)
-   [Registrierungsschlüssel und-Werte](#registry-keys-and-values)
-   [Konfigurieren eines Anbieters für die Durchführung im sicheren oder kompatiblen Modus](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Sicherer und kompatibler Modus

Ab Windows 7 wurden die folgenden zwei laufenden Modi für den freigegebenen WMI-Host Prozess hinzugefügt:

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Sicherer Modus
</dt> <dd>

Die Prozess Ressourcen des WMI-Anbieter Hosts sind mit einer [*Dienst-SID*](gloss-s.md)gesichert. Nur die *Dienst-SID* verfügt über Berechtigungen für diese Ressourcen.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Kompatibler Modus
</dt> <dd>

Der Host Prozess für den freigegebenen WMI-Anbieter ist nicht mit einer [*Dienst-SID*](gloss-s.md)gesichert. Der Anbieter Host Prozess ermöglicht den Zugriff auf die Konten Network Service oder LocalService, abhängig vom Hostingmodell. Weitere Informationen zum Hosting von Modellen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

</dd> </dl>

**Windows Vista und Windows Server 2008:** Um auf die Registrierungsschlüssel und-Werte zum Steuern des sicheren und kompatiblen Modus für den Anbieter Host Prozess zuzugreifen, müssen Sie das Sicherheitsupdate in [KB 959454](https://support.microsoft.com/kb/959454)installieren. Weitere Informationen finden Sie im [Microsoft-Sicherheits Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).

## <a name="registry-keys-and-values"></a>Registrierungsschlüssel und-Werte

Die Einstellungen für den sicheren und kompatiblen Modus werden über Registrierungsschlüssel angegeben. Die Registrierungsschlüssel für WMI befinden sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

Die folgenden Registrierungsschlüssel und **DWORD** -Werte, die in der folgenden Liste beschrieben werden, wurden hinzugefügt, um das Verhalten von WMI-Anbietern zu steuern.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**Securedhostproviders**
</dt> <dd>

Dieser Schlüssel steuert das Verhalten einzelner Anbieter. Alle Anbieter, die in diesem Schlüssel aufgelistet sind, werden immer im sicheren Modus ausgeführt. Alle Eingangsbox Anbieter, die mit Windows ausgeliefert werden, sind unter diesem Schlüssel aufgeführt und werden standardmäßig im sicheren Modus ausgeführt.

Dieser Schlüssel hat Vorrang vor Anbietern, die im Schlüssel **compatiblehostproviders** aufgeführt sind.

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**Compatiblehostproviders**
</dt> <dd>

Dieser Schlüssel steuert das Verhalten einzelner Anbieter. Alle Anbieter, die in diesem Schlüssel aufgelistet sind, werden immer im kompatiblen Modus ausgeführt. Dieser Schlüssel ist standardmäßig leer.

Wenn ein Anbieter im Schlüssel **securedhostproviders** und im Schlüssel **compatiblehostproviders** aufgeführt ist, wird der Anbieter im sicheren Modus ausgeführt.

> [!Note]  
> Der Schlüssel **compatiblehostproviders** bietet Anwendungs Kompatibilität für Anwendungen von Drittanbietern, wenn der **DefaultSecuredHost** -Schlüssel auf 1 festgelegt ist und der Anbieter bekanntermaßen nicht im sicheren Modus funktioniert.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Ein globaler **DWORD** -Registrierungs Wert, der bestimmt, ob alle Anbieter, die nicht in den Schlüsseln **securedhostproviders** oder **compatiblehostproviders** aufgeführt sind, im sicheren oder kompatiblen Modus ausgeführt werden. Dieser **DWORD** -Wert ermöglicht dem Administrator, den Modus zu entscheiden, der von einem Drittanbieter ausgeführt werden muss. Standardmäßig ist dieser Wert auf 0 (null) festgelegt, und alle Drittanbieter Anbieter werden im kompatiblen Modus ausgeführt. Administratoren können Ihren Computer standardmäßig sicherer machen, indem Sie den **DefaultSecuredHost** -Wert auf "1" festlegen.

> [!Note]  
> Der **DefaultSecuredHost** -Wert hat keine Auswirkung auf die anderen Registrierungsschlüssel. Die im **securedhostproviders** -Schlüssel aufgelisteten Anbieter bleiben im sicheren Modus, und die im **Kompatibilitäts Hostproviders** -Schlüssel aufgeführten Anbieter bleiben im kompatiblen Modus.

 

Folgende Einstellungen sind möglich:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Gibt an, dass Anbieter im kompatiblen Modus ausgeführt werden.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Gibt an, dass Anbieter im sicheren Modus ausgeführt werden.

</dd> </dl> </dd> </dl>

In der folgenden Liste sind die möglichen Registrierungs Einstellungen und die zugehörigen laufenden Modi für einen Anbieter aufgelistet.



| Unter securedhostproviders aufgeführt | Unter compatiblehostproviders aufgeführt | DefaultSecuredHost-Einstellung | Mode       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| Nein                                | Nein                                   | 0                          | Kompatibel |
| Nein                                | Ja                                  | 0                          | Kompatibel |
| Ja                               | Nein                                   | 0                          | Sicher     |
| Ja                               | Ja                                  | 0                          | Sicher     |
| Nein                                | Nein                                   | 1                          | Sicher     |
| Nein                                | Ja                                  | 1                          | Kompatibel |
| Ja                               | Nein                                   | 1                          | Sicher     |
| Ja                               | Ja                                  | 1                          | Sicher     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Konfigurieren eines Anbieters für die Durchführung im sicheren oder kompatiblen Modus

Die Registrierungsschlüssel können mithilfe der Gruppenrichtlinien-Verwaltungskonsole (GPMC) geändert werden. Weitere Informationen finden Sie unter [Gruppenrichtlinien-Verwaltungskonsole](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Die folgenden Verfahren veranschaulichen, wie Sie Einstellungen für den sicheren und kompatiblen Modus mithilfe von Gruppenrichtlinien Einstellungen verwalten. Weitere Informationen zu Gruppenrichtlinien Einstellungen finden Sie in der [Übersicht über Gruppenrichtlinie Einstellungen](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).

**So fügen Sie dem sicheren oder kompatiblen Modus einen Anbieter mithilfe von Gruppenrichtlinie hinzu**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinie Objekt (GPO).
3.  Bearbeiten Sie das Gruppenrichtlinien Objekt.
4.  Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**. Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den Befehl **Erstellen** aus.
7.  Wählen Sie den folgenden Registrierungsschlüssel Pfad aus:

    **Sicherer Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **securedhostproviders**

    **Kompatibler Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **compatiblehostproviders**

8.  Geben Sie im Feld **Name** den Namen des Anbieters ein, den Sie diesem Schlüssel hinzufügen möchten. Der Anbieter Name muss das folgende Format aufweisen: <namespace> : <\_ \_ RelPath>. Beispiel \\ : root cimv2: \_ \_ win32provider. Name = "MyProvider".
9.  Geben Sie im Feld **Daten** den Wert 0 ein.
10. Klicken Sie auf OK.

**So entfernen Sie einen Anbieter aus dem sicheren oder kompatiblen Modus mithilfe von Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinien Objekt.
3.  Bearbeiten Sie das Gruppenrichtlinien Objekt.
4.  Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**. Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den Befehl **Entfernen** aus.
7.  Wählen Sie den folgenden Registrierungsschlüssel Pfad aus:

    **Sicherer Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **securedhostproviders**

    **Kompatibler Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **compatiblehostproviders**

8.  Geben Sie im Feld **Name** den Namen des Anbieters ein, den Sie aus diesem Schlüssel entfernen möchten.
9.  Geben Sie im Feld **Daten** den Wert 0 ein.
10. Klicken Sie auf OK.

Das folgende Verfahren enthält Details zum Ändern des Verhaltens von Anbietern, die nicht in den Schlüsseln **securedhostproviders** oder **compatiblehostproviders** aufgeführt sind.

**So ändern Sie den Standardwert des Schlüssels DefaultSecuredHost mithilfe von Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinien Objekt.
3.  Bearbeiten Sie das Gruppenrichtlinien Objekt.
4.  Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**. Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den Befehl **Aktualisieren** aus.
7.  Wählen Sie den folgenden Registrierungsschlüssel Pfad aus: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  Geben Sie im Feld **Name den Namen** **DefaultSecuredHost** ein.
9.  Geben Sie im Feld **Daten** den Wert 0 für den kompatiblen Modus oder 1 für den sicheren Modus ein.
10. Klicken Sie auf OK.

 

 
