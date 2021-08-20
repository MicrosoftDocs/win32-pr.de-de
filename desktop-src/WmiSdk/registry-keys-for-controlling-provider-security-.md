---
description: Um die Sicherheit des hostprozesses (wmiprvse.exe) der Windows-Verwaltungsinstrumentation (WMI) zu erhöhen, wurden Änderungen an Windows-Plattformen vorgenommen, die den Anbieterhostprozess mit einer Dienstsicherheits-ID (SID) sichern.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Registrierungsschlüssel und -werte zum Steuern der Anbietersicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8695f8203a56a934aa7d0f579b6a43f36d2ce7342a15b0bb408ff8696a7e8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817088"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Registrierungsschlüssel und -werte zum Steuern der Anbietersicherheit

Um die Sicherheit des WMI-Hostprozesses (wmiprvse.exe) der Windows-Verwaltungsinstrumentation (WMI) zu erhöhen, wurden Änderungen an Windows-Plattformen vorgenommen, die den Anbieterhostprozess mit einer Dienstsicherheits-ID [*(SID) sichern.*](gloss-s.md) Diese Änderungen führen zu den folgenden Ausführungsmodi für den freigegebenen WMI-Host: sicher und kompatibel.

Die folgenden Abschnitte werden in diesem Thema behandelt:

-   [Sicherer und kompatibler Modus](#secure-and-compatible-modes)
-   [Registrierungsschlüssel und -werte](#registry-keys-and-values)
-   [Konfigurieren eines Anbieters für die Ausführung im sicheren oder kompatiblen Modus](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Sicherer und kompatibler Modus

Ab Windows 7 wurden die folgenden beiden Ausführungsmodi für den WMI-Prozess für freigegebene Hosts hinzugefügt:

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Sicherer Modus
</dt> <dd>

Hostprozessressourcen des WMI-Anbieters werden mit einer [*Dienst-SID geschützt.*](gloss-s.md) Nur die *Dienst-SID* verfügt über Berechtigungen für diese Ressourcen.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Kompatibler Modus
</dt> <dd>

Der WMI-Hostprozess für freigegebene Anbieter ist nicht mit einer [*Dienst-SID gesichert.*](gloss-s.md) Der Anbieterhostprozess ermöglicht abhängig vom Hostingmodell den Zugriff auf die Konten NetworkService oder LocalService. Weitere Informationen zum Hosten von Modellen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

</dd> </dl>

**Windows Vista und Windows Server 2008:** Um auf die Registrierungsschlüssel und -werte zum Steuern sicherer und kompatibler Modi für den Anbieterhostprozess zu zugreifen, müssen Sie das Sicherheitsupdate in [KB](https://support.microsoft.com/kb/959454)959454. Weitere Informationen finden Sie im [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).

## <a name="registry-keys-and-values"></a>Registrierungsschlüssel und -werte

Die Einstellungen für den sicheren und kompatiblen Modus werden über Registrierungsschlüssel angegeben. Die Registrierungsschlüssel für WMI befinden sich in der Registrierung unter **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

Die folgenden Registrierungsschlüssel und der in der folgenden Liste beschriebene **DWORD-Wert** wurden hinzugefügt, um das Verhalten von WMI-Anbietern zu steuern.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

Dieser Schlüssel steuert das Verhalten einzelner Anbieter. Alle Anbieter, die in diesem Schlüssel aufgeführt sind, werden immer im sicheren Modus ausgeführt. Alle Posteingangsanbieter, die mit Windows geliefert werden, sind unter diesem Schlüssel aufgeführt und werden standardmäßig im sicheren Modus ausgeführt.

Dieser Schlüssel hat Vorrang vor Anbietern, die im **Schlüssel CompatibleHostProviders aufgeführt** sind.

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

Dieser Schlüssel steuert das Verhalten einzelner Anbieter. Alle Anbieter, die in diesem Schlüssel aufgeführt sind, werden immer im kompatiblen Modus ausgeführt. Dieser Schlüssel ist standardmäßig leer.

Wenn ein Anbieter sowohl im **SecuredHostProviders-Schlüssel** als auch im **CompatibleHostProviders-Schlüssel** aufgeführt ist, wird der Anbieter im sicheren Modus ausgeführt.

> [!Note]  
> Der **Schlüssel CompatibleHostProviders** bietet Anwendungskompatibilität für Drittanbieteranwendungen, wenn **der DefaultSecuredHost-Schlüssel** auf 1 festgelegt ist und der Anbieter bekannterweise nicht im sicheren Modus funktioniert.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Ein **DWORD-Wert** für die globale Registrierung, der bestimmt, ob alle Anbieter, die nicht in den **Schlüsseln SecuredHostProviders** oder **CompatibleHostProviders** aufgeführt sind, im sicheren oder kompatiblen Modus ausgeführt werden. Mit **diesem DWORD-Wert** kann der Administrator entscheiden, unter welchem Modus ein Drittanbieter ausgeführt werden muss. Standardmäßig ist dieser Wert auf 0 (null) festgelegt, und alle Drittanbieter werden im kompatiblen Modus ausgeführt. Administratoren können ihren Computer standardmäßig sicherer machen, indem sie **den DefaultSecuredHost-Wert** auf 1 festlegen.

> [!Note]  
> Der **DefaultSecuredHost-Wert** wirkt sich nicht auf die anderen Registrierungsschlüssel aus. Die anbieter, die im **SecuredHostProviders-Schlüssel** aufgeführt sind, verbleiben im sicheren Modus, und die im **Schlüssel CompatibleHostProviders** aufgelisteten Anbieter bleiben im kompatiblen Modus.

 

Die folgenden Einstellungen sind möglich:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Gibt an, dass Anbieter im kompatiblen Modus ausgeführt werden.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Gibt an, dass Anbieter im sicheren Modus ausgeführt werden.

</dd> </dl> </dd> </dl>

In der folgenden Liste sind die möglichen Registrierungseinstellungen und die zugeordneten Ausführungsmodi für einen Anbieter aufgeführt.



| Aufgeführt unter SecuredHostProviders | Aufgeführt unter CompatibleHostProviders | DefaultSecuredHost-Einstellung | Mode       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| Nein                                | Nein                                   | 0                          | Kompatibel |
| Nein                                | Ja                                  | 0                          | Kompatibel |
| Ja                               | Nein                                   | 0                          | Sicher     |
| Ja                               | Ja                                  | 0                          | Sicher     |
| Nein                                | Nein                                   | 1                          | Sicher     |
| Nein                                | Ja                                  | 1                          | Kompatibel |
| Ja                               | Nein                                   | 1                          | Sicher     |
| Ja                               | Ja                                  | 1                          | Sicher     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Konfigurieren eines Anbieters für die Ausführung im sicheren oder kompatiblen Modus

Die Registrierungsschlüssel können mithilfe der Gruppenrichtlinien-Verwaltungskonsole (GPMC) geändert werden. Weitere Informationen finden Sie unter [Gruppenrichtlinien-Verwaltungskonsole](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Die folgenden Verfahren veranschaulichen, wie Einstellungen für den sicheren und kompatiblen Modus mithilfe von Gruppenrichtlinieneinstellungen verwaltet werden. Weitere Informationen zu Gruppenrichtlinieneinstellungen finden Sie unter Gruppenrichtlinie Preferences Overview (Übersicht [über Gruppenrichtlinie Einstellungen).](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11))

**So fügen Sie einen Anbieter entweder dem sicheren oder kompatiblen Modus hinzu, indem Sie Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie Gruppenrichtlinie -Objekt (GPO).
3.  Bearbeiten Sie das Gruppenrichtlinienobjekt.
4.  Navigieren Sie zu Einstellungen/Windows Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **Neu... aus. Registrierung**. Diese Aktion stellt eine Benutzeroberfläche bereit, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den **Befehl Erstellen** aus.
7.  Wählen Sie den folgenden Registrierungsschlüsselpfad aus:

    **Sicherer Modus: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Kompatibler Modus: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  Geben Sie **im Feld** Name den Namen des Anbieters ein, den Sie diesem Schlüssel hinzufügen möchten. Der Anbietername muss das folgende Format haben: <namespace> :<\_ \_ RELPATH>. Beispiel: root \\ cimv2: \_ \_ win32provider.name="MyProvider".
9.  Geben Sie **im Datenfeld** 0 ein.
10. Klicken Sie auf OK.

**So entfernen Sie einen Anbieter aus dem sicheren oder kompatiblen Modus mit Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinienobjekt.
3.  Bearbeiten Sie das Gruppenrichtlinienobjekt.
4.  Navigieren Sie zu Einstellungen/Windows Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **Neu... aus. Registrierung**. Diese Aktion stellt eine Benutzeroberfläche bereit, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den **Befehl Entfernen** aus.
7.  Wählen Sie den folgenden Registrierungsschlüsselpfad aus:

    **Sicherer Modus: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Kompatibler Modus: HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  Geben Sie **im Feld** Name den Namen des Anbieters ein, den Sie aus diesem Schlüssel entfernen möchten.
9.  Geben Sie **im Datenfeld** 0 ein.
10. Klicken Sie auf OK.

Das folgende Verfahren enthält Details zum Ändern des Verhaltens von Anbietern, die nicht in den **Schlüsseln SecuredHostProviders** oder **CompatibleHostProviders aufgeführt** sind.

**So ändern Sie den Standardwert des DefaultSecuredHost-Schlüssels mithilfe Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinienobjekt.
3.  Bearbeiten Sie das Gruppenrichtlinienobjekt.
4.  Navigieren Sie zu Einstellungen/Windows Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **Neu... aus. Registrierung**. Diese Aktion stellt eine Benutzeroberfläche bereit, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den **Befehl Aktualisieren** aus.
7.  Wählen Sie den folgenden Registrierungsschlüsselpfad aus: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  Geben Sie **im Feld Name** den Namen **DefaultSecuredHost ein.**
9.  Geben Sie **im Datenfeld** 0 für den kompatiblen Modus oder 1 für den sicheren Modus ein.
10. Klicken Sie auf OK.

 

 
