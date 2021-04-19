---
title: MDM_WindowsLicensing-Klasse
description: Die MDM- \_ windowslicensing-Klasse ist für Lizenzierungs bezogene Verwaltungs Szenarien konzipiert.
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
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341791"
---
# <a name="mdm_windowslicensing-class"></a>MDM- \_ windowslicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM- \_ windowslicensing** -Klasse ist für Lizenzierungs bezogene Verwaltungs Szenarien konzipiert. Derzeit ist der Bereich auf Editions Upgrades von Windows 10-Desktop Computern und mobilen Geräten wie Windows 10 pro auf Windows 10 Enterprise beschränkt. Außerdem bietet dieser CSP die Möglichkeit, die Product Key von Windows 10-Desktop Geräten zu aktivieren oder zu ändern.

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

Die **MDM \_ windowslicensing** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MDM \_ windowslicensing** -Klasse verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>Changeproductkeymethod</strong></a></td>
<td style="text-align: left;">Installiert eine Product Key für Windows 10 Desktop-Geräte. Wird nicht neu gestartet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>Checkapplicabilitymethod</strong></a></td>
<td style="text-align: left;">Methode, um zu überprüfen, ob der eingegebene Product Key für ein Editions Upgrade, eine Aktivierung oder Änderung eines Product Key von Windows 10 für Desktop Geräte verwendet werden kann.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>Upgradeeditionwithlicenermethod</strong></a></td>
<td style="text-align: left;">Stellen Sie eine Lizenz für ein Editions Upgrade von Windows 10 Mobile-Geräten bereit.<br/>
<blockquote>
[!Note]<br />
Für diesen Upgradevorgang ist kein Systemneustart erforderlich.
</blockquote>
<br/> <br/> Der Date-Typ ist "XML".<br/> Der unterstützte Vorgang ist "Execute".<br/>
<blockquote>
[!Important]<br />
Der Inhalt der XML-Lizenzdatei muss ordnungsgemäß mit Escapezeichen versehen werden (d. h. es sollte nicht einfach ein kopierter XML-Code sein). andernfalls tritt bei der Editions Aktualisierung auf Windows 10 Mobile-Geräten Weitere Informationen zum ordnungsgemäßen Escapezeichen der XML-Lizenzdatei finden Sie im Abschnitt 2,4 der <a href="https://www.w3.org/TR/xml/">W3C-XML-Spezifikation</a>. Die XML-Lizenzdatei wird vom Microsoft Volume Licensing Service Center abgerufen. Ihre Organisation muss über einen Volumenlizenzvertrag mit Microsoft verfügen, um auf das Portal zugreifen zu können.
</blockquote>
<br/> Im folgenden sind gültige Editions Upgradepfade aufgeführt, wenn dieser Knoten über ein MDM-oder Bereitstellungs Paket verwendet wird:
<ul>
<li>Windows 10 mobileto Windows 10 Mobile Enterprise<br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>Upgradeeditionwithproductkeymethod</strong></a></td>
<td style="text-align: left;">Hiermit wird das Gerät ausgelöst, um die Product Key zu übernehmen und die Edition des Clients zu aktualisieren.
<blockquote>
[!Note]<br />
Dieser Upgradevorgang erfordert einen Systemneustart.
</blockquote>
<br/> <br/> Der unterstützte Vorgang ist "Execute".<br/> Wenn ein Product Key von einem MDM-Server an das Gerät eines Benutzers übermittelt wird, wird <strong>changepk.exe</strong> mithilfe der Product Key ausgeführt. Nachdem der Vorgang abgeschlossen ist, wird dem Benutzer eine Benachrichtigung angezeigt, dass eine neue Edition von Windows 10 verfügbar ist. Der Benutzer kann dann das System manuell neu starten, oder nach zwei Stunden wird das Gerät automatisch neu gestartet, um das Upgrade abzuschließen. Der Benutzer erhält eine Erinnerungs Benachrichtigung 10 Minuten vor dem automatischen Neustart.<br/> Nachdem das Gerät neu gestartet wurde, wird der Editions Upgradevorgang abgeschlossen. Der Benutzer erhält eine Benachrichtigung über das erfolgreiche Upgrade.
<blockquote>
[!Important]<br />
Wenn eine andere Richtlinie einen Systemneustart erfordert, der auftritt, wenn <strong>changepk.exe</strong> ausgeführt wird, kann das Editions Upgrade nicht ausgeführt werden.
</blockquote>
<br/> <br/> Wenn ein Product Key in einem Bereitstellungs Paket eingegeben wird und der Benutzer mit der Installation des Pakets beginnt, wird dem Benutzer eine Benachrichtigung angezeigt, dass das System neu gestartet wird, um die Paketinstallation abzuschließen. Nach der expliziten Zustimmung des Benutzers, um den Vorgang fortzusetzen, setzt das Paket die Installation fort und <strong>changepk.exe</strong> mithilfe des Product Key ausgeführt. Der Benutzer erhält eine Erinnerungs Benachrichtigung 30 Sekunden vor dem automatischen Neustart. <br/> Nachdem das Gerät neu gestartet wurde, wird der Editions Upgradevorgang abgeschlossen. Der Benutzer erhält eine Benachrichtigung über das erfolgreiche Upgrade. <br/> Dieser Knoten kann auch verwendet werden, um eine Product Key einer bestimmten Edition des Windows 10-Desktop Geräts zu aktivieren oder zu ändern, indem Sie eine Product Key eingeben. Für das Aktivieren oder Ändern einer Product Key ist kein Neustart erforderlich, und es handelt sich um einen unbeaufsichtigten Prozess für den Benutzer.<br/>
<blockquote>
[!Important]<br />
Der eingegebene Product Key muss 29 Zeichen umfassen (d. h., er sollte Bindestriche enthalten), andernfalls tritt bei der Aktivierung, dem Editions Upgrade oder der Product Key Änderung auf Windows 10-Desktop Geräten ein Fehler auf. Der Product Key wird von Microsoft Volume Licensing Service Center abgerufen. Ihre Organisation muss über einen Volumenlizenzvertrag mit Microsoft verfügen, um auf das Portal zugreifen zu können.
</blockquote>
<br/> Im folgenden finden Sie gültige Editions Upgradepfade, wenn dieser Knoten über eine MDM verwendet wird:
<ul>
<li>Windows 10 Enterprise zu Windows 10 Education</li>
<li>Windows 10 Home zu Windows 10 Education</li>
<li>Windows 10 pro zu Windows 10 Education</li>
<li>Windows 10 pro zu Windows 10 Enterprise</li>
</ul>
<br/> Die Aktivierung oder Änderung einer Product Key kann für die folgenden Editionen ausgeführt werden:
<ul>
<li>Windows 10 Education</li>
<li>Windows 10 Enterprise</li>
<li>Windows 10 Home</li>
<li>Windows 10 Pro</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ windowslicensing** -Klasse verfügt über diese Eigenschaften.

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

Gibt den Namen des übergeordneten Knotens an.

</dd> <dt>

[Licentkeytype](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

