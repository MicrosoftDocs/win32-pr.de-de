---
title: MDM_WindowsLicensing-Klasse
description: Die MDM \_ WindowsLicensing-Klasse ist für lizenzierungsbezogene Verwaltungsszenarien konzipiert.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9470b72cb6a50323af9294be4a6506682fc7aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480926"
---
# <a name="mdm_windowslicensing-class"></a>MDM \_ WindowsLicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ WindowsLicensing-Klasse** ist für lizenzierungsbezogene Verwaltungsszenarien konzipiert. Derzeit ist der Bereich auf Editionsupgrades Windows 10 Desktop- und mobilen Geräten beschränkt, z. B. Windows 10 Pro auf Windows 10 Enterprise. Darüber hinaus bietet dieser CSP die Möglichkeit zum Aktivieren oder Ändern des Product Key Windows 10 Desktopgeräten.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a>Member

Die **MDM \_ WindowsLicensing-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MDM \_ WindowsLicensing-Klasse** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a> | Installiert einen Product Key für Windows 10 Desktopgeräte. Wird nicht neu gestartet.<br /> | 
| <a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a> | Methode, um zu überprüfen, ob der eingegebene Product Key für ein Editionsupgrade, die Aktivierung oder das Ändern eines Product Key von Windows 10 Desktopgeräten verwendet werden kann.<br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a> | Stellen Sie eine Lizenz für ein Editionsupgrade Windows 10 mobilen Geräten zur Verfügung.<br /><blockquote>[!Note]<br />Für diesen Upgradeprozess ist kein Systemneustart erforderlich.</blockquote><br /><br /> Der Datumstyp ist XML.<br /> Der unterstützte Vorgang ist Execute.<br /><blockquote>[!Important]<br />Der Inhalt der XML-Lizenzdatei muss ordnungsgemäß mit Escapeinformationen geschützt werden (d. h. es sollte sich nicht einfach um eine kopierte XML-Datei handelt). Andernfalls wird das Editionsupgrade auf Windows 10 mobilen Geräten fehlschlagen. Weitere Informationen zum richtigen Verwenden von Caping für die XML-Lizenzdatei finden Sie in Abschnitt 2.4 der <a href="https://www.w3.org/TR/xml/">W3C-XML-Spezifikation.</a> Die XML-Lizenzdatei wird aus dem Microsoft Volume Licensing Service Center erworben. Ihre Organisation muss über einen Volumenlizenzvertrag mit Microsoft verfügen, um auf das Portal zugreifen zu können.</blockquote><br /> Im Folgenden finden Sie gültige Editionsupgradepfade, wenn Sie diesen Knoten über ein MDM- oder Bereitstellungspaket verwenden:<ul><li>Windows 10 Mobileto Windows 10 Mobile Enterprise<br /></li></ul><br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a> | Löst das Gerät aus, um den Product Key zu übernehmen und die Edition des Clients zu aktualisieren.<blockquote>[!Note]<br />Dieser Upgradevorgang erfordert einen Systemneustart.</blockquote><br /><br /> Der unterstützte Vorgang ist Execute.<br /> Wenn ein Product Key von einem MDM-Server auf das Gerät eines Benutzers übertragen <strong> wird, </strong>changepk.exemit dem Product Key ausgeführt. Nach Abschluss wird dem Benutzer eine Benachrichtigung angezeigt, dass eine neue Edition Windows 10 verfügbar ist. Der Benutzer kann sein System dann manuell neu starten, oder nach zwei Stunden wird das Gerät automatisch neu gestartet, um das Upgrade abschließen zu können. Der Benutzer erhält 10 Minuten vor dem automatischen Neustart eine Erinnerungsbenachrichtigung.<br /> Nach dem Neustart des Geräts wird das Editionsupgrade abgeschlossen. Der Benutzer erhält eine Benachrichtigung über das erfolgreiche Upgrade.<blockquote>[!Important]<br />Wenn eine andere Richtlinie einen Systemneustart erfordert, der beichangepk.exeausgeführt wird, tritt beim Editionsupgrade ein Fehler auf. <strong></strong></blockquote><br /><br /> Wenn ein Product Key in ein Bereitstellungspaket eingegeben wird und der Benutzer mit der Installation des Pakets beginnt, wird dem Benutzer eine Benachrichtigung angezeigt, dass sein System neu gestartet wird, um die Paketinstallation abzuschließen. Nach der expliziten Zustimmung des Benutzers zum Fortfahren setzt das Paket die Installation fort <strong> undchangepk.exe</strong> mit dem Product Key ausgeführt werden. Der Benutzer erhält 30 Sekunden vor dem automatischen Neustart eine Erinnerungsbenachrichtigung. <br /> Nach dem Neustart des Geräts wird das Editionsupgrade abgeschlossen. Der Benutzer erhält eine Benachrichtigung über das erfolgreiche Upgrade. <br /> Dieser Knoten kann auch verwendet werden, um einen Product Key auf einer bestimmten Edition von Windows 10 Desktopgerät durch Eingabe eines Product Key zu aktivieren oder zu ändern. Die Aktivierung oder Änderung eines Product Key erfordert keinen Neustart und ist ein automatischer Prozess für den Benutzer.<br /><blockquote>[!Important]<br />Der eingegebene Product Key muss aus 29 Zeichen bestehen (d.h. er sollte Bindestriche enthalten), andernfalls kann die Aktivierung, das Editionsupgrade oder die Änderung des Product Key auf Windows 10 Desktopgeräten nicht ausgeführt werden. Der Product Key wird vom Microsoft Volume Licensing Service Center erworben. Ihre Organisation muss über einen Volumenlizenzvertrag mit Microsoft verfügen, um auf das Portal zugreifen zu können.</blockquote><br /> Im Folgenden finden Sie gültige Editionsupgradepfade, wenn Sie diesen Knoten über eine MDM verwenden:<ul><li>Windows 10 Enterprise, um Windows 10 Education</li><li>Windows 10 Home sie Windows 10 Education</li><li>Windows 10 Pro sie Windows 10 Education</li><li>Windows 10 Pro sie Windows 10 Enterprise</li></ul><br /> Die Aktivierung oder Änderung eines Product Key kann in den folgenden Editionen durchgeführt werden:<ul><li>Windows 10 Education</li><li>Windows 10 Enterprise</li><li>Windows 10 Home</li><li>Windows 10 Pro</li></ul><br /> | 




 

### <a name="properties"></a>Eigenschaften

Die **MDM \_ WindowsLicensing-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[Edition](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens.

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/".

</dd> <dt>

[Status](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | \\Stamm-CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

