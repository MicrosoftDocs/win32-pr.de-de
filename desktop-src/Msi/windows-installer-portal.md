---
description: Installer-Engine zum Installieren von Anwendungen oder Updates oder-Diensten, die unter Windows ausgeführt werden. Hiermit werden installierte Anwendungen konfiguriert und repariert. Schreiben Sie benutzerdefinierte MSI-Pakete, um eine exe-Setup Installation oder ein Update oder Upgrade für eine Anwendung zu erstellen.
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: d818a3decc7cbede527929dc3756ba2edf193421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360625"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> Diese Dokumentation ist für Softwareentwickler gedacht, die Windows Installer verwenden möchten, um Installer-Pakete für Anwendungen zu erstellen. Wenn Sie nach einem verteilbaren verteilbaren Windows Installer 4,5 und früher suchen, finden Sie weitere Informationen in [diesem Artikel](windows-installer-redistributables.md). Beachten Sie, dass es für Windows Installer 5,0 keine verteilbare verteilbare Tabelle gibt. Diese Version ist im Betriebssystem in Windows 7, Windows Server 2008 R2 und späteren Client-und Server Releases (einschließlich Windows 10) enthalten.

Microsoft Windows Installer ist ein Installations-und Konfigurations Dienst, der mit Windows bereitgestellt wird. Der Installer-Dienst ermöglicht es Kunden, eine bessere Unternehmens Bereitstellung bereitzustellen und ein Standardformat für die Komponenten Verwaltung bereitzustellen. Das Installationsprogramm ermöglicht außerdem die Ankündigung von Anwendungen und Features gemäß dem Betriebssystem. Weitere Informationen finden Sie unter [Platt Form Unterstützung für Werbung](platform-support-of-advertisement.md).

In dieser Dokumentation werden Windows Installer 5,0 und frühere Versionen beschrieben. Nicht alle Funktionen, die in späteren Versionen von Windows Installer verfügbar sind, sind in früheren Versionen verfügbar. In dieser Dokumentation werden keine früheren Versionen als Windows Installer 2,0 beschrieben. Installationspakete und Patches, die für Windows Installer 2,0 erstellt werden, können weiterhin mit Windows Installer 3,0 und höher installiert werden.

Windows Installer 3,0 und höher kann mehrere Patches mit einer einzelnen Transaktion installieren, mit der der Installationsfortschritt, Rollback und Neustarts integriert werden. Das Installationsprogramm kann Patches in einer angegebenen Reihenfolge anwenden, unabhängig von der Reihenfolge, in der die Patches dem System bereitgestellt werden. Beim Patchen mit Windows Installer 3,0 werden nur die Dateien aktualisiert, die vom Patch betroffen sind, und Sie können erheblich schneller sein als frühere Installer-Versionen. Patches, die mit Windows Installer 3,0 oder höher installiert werden, können in beliebiger Reihenfolge deinstalliert werden, um den Zustand des Produkts unverändert zu lassen, wenn der Patch nie installiert wurde. Konten mit Administratorrechten können die API von Windows Installer 3,0 und höher verwenden, um Produkt-, Funktions-, Komponenten-und Patchinformationen abzufragen und zu inventarisieren. Das Installationsprogramm kann verwendet werden, um Quell Listen für Netzwerk-, URL-und Medienquellen zu lesen, zu bearbeiten und zu ersetzen. Administratoren können Benutzer-und Installations Kontexte aufzählen und Quell Listen über einen externen Prozess verwalten.

Windows Installer 4,5 und höher können mehrere Installationspakete mithilfe der [*Transaktionsverarbeitung*](t-gly.md)installieren. Wenn alle Pakete in der Transaktion nicht erfolgreich installiert werden können oder wenn der Benutzer die Installation abbricht, kann die Windows Installer Änderungen zurücksetzen und den ursprünglichen Zustand des Computers wiederherstellen. Das Installationsprogramm stellt sicher, dass alle Pakete, die zu einer Transaktion mit mehreren Paketen gehören, installiert sind oder keines der Pakete installiert ist.

Ab Windows Installer 5,0 kann ein Paket erstellt werden, um neue Konten, Windows- [Dienste](../services/services.md), Dateien, Ordner und Registrierungsschlüssel zu sichern. Das Paket kann eine Sicherheits Beschreibung angeben, die Berechtigungen ablehnt, die Vererbung von Berechtigungen für eine übergeordnete Ressource angibt oder die Berechtigungen eines neuen Kontos angibt. Weitere Informationen finden Sie unter [Sichern von Ressourcen](securing-resources-.md). Der Windows Installer 5,0-Dienst kann alle auf dem Computer installierten Komponenten auflisten und den Schlüssel Pfad für die Komponente abrufen. Weitere Informationen finden Sie unter [Enumerieren von Komponenten](enumerating-components-.md). [Mithilfe der Dienst Konfiguration](using-services-configuration.md)können Windows Installer 5,0-Pakete die Dienste auf einem Computer anpassen. Setup Entwickler können mit Windows Installer 5,0 und einer [einzelnen Paket Erstellung](single-package-authoring.md) einzelne Installationspakete entwickeln, mit denen eine Anwendung entweder im Computer-oder benutzerspezifischen [Installations Kontext](installation-context.md)installiert werden kann.

## <a name="where-applicable"></a>Anwendungsbereich

Windows Installer ermöglicht die effiziente Installation und Konfiguration von Produkten und Anwendungen, die unter Windows ausgeführt werden. Das Installationsprogramm bietet neue Funktionen zum Ankündigen von Features, ohne Sie zu installieren, Produkte bei Bedarf zu installieren und benutzerdefinierte Anpassungen hinzuzufügen.

Windows Installer 5,0, die unter Windows Server 2012 oder Windows 8 ausgeführt wird, unterstützt die Installation genehmigter apps auf Windows RT. Ein Windows Installer Paket, ein Patch oder eine Transformation, die nicht von Microsoft signiert wurde, kann unter Windows RT nicht installiert werden. Die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft gibt die Plattform an, die mit einer Installations Datenbank kompatibel ist, und sollte in diesem Fall den Wert für Windows RT enthalten.

Windows Installer ist für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation ist für Softwareentwickler gedacht, die Anwendungen erstellen möchten, die Windows Installer verwenden. Es enthält allgemeine Hintergrundinformationen zu Installationspaketen und zum Installerdienst. Sie enthält eine umfassende Beschreibung der Anwendungsprogrammierschnittstelle und der Elemente der Installer-Datenbank. Diese Dokumentation enthält auch ergänzende Informationen für Entwickler, die einen Tabellen-Editor oder ein Paket Erstellungs Tool verwenden möchten, um eine Installation zu erstellen oder zu verwalten.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Windows Installer 5,0 ist in, Windows 7, Windows Server 2008 R2 und späteren Versionen enthalten. Es ist kein verteilbares für Windows Installer 5,0 vorhanden.

Frühere Versionen als Windows Installer 5,0 wurden mit Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP und Windows 2000 veröffentlicht. [Windows Installer Redistributables](windows-installer-redistributables.md) sind für Windows Installer 4,5 und einige frühere Versionen verfügbar.

* Windows Installer 4,5 erfordert Windows Server 2008, Windows Vista, Windows XP mit Service Pack 2 (SP2) und höher und Windows Server 2003 mit Service Pack 1 (SP1) und höher.

* Windows Installer 4,0 erfordert Windows Vista oder Windows Server 2008. Es gibt keine weitervertreibbare Komponente zum Installieren von Windows Installer 4,0 unter anderen Betriebssystemen. In Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 ist eine aktualisierte Version von Windows Installer 4,0 verfügbar, von der keine neuen Features hinzugefügt werden.

* Windows Installer 3,1 erfordert Windows Server 2003, Windows XP oder Windows 2000 mit Service Pack 3 (SP3).

* Windows Installer 3,0 erfordert Windows Server 2003, Windows XP oder Windows 2000 mit SP3. Windows Installer 3,0 ist in Windows XP mit Service Pack 2 (SP2) enthalten. Es ist als verteilbare Komponente für Windows 2000 Server mit Service Pack 3 (SP3) und Windows 2000 Server mit Service Pack 4 (SP4), Windows XP RTM und Windows XP mit Service Pack 1 (SP1) und Windows Server 2003 RTM verfügbar.

* Windows Installer 2,0 ist in Windows Server 2003 und Windows XP enthalten.

* Windows Installer 2,0 ist als Paket für die Installation oder das Upgrade auf Windows Installer 2,0 unter Windows 2000 verfügbar. Dieses Paket sollte nicht für die Installation oder das Upgrade von Windows Installer 2,0 unter Windows Server 2003 und Windows XP verwendet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Roadmap](roadmap-to-windows-installer-documentation.md)<br/>                        | Eine Anleitung für Windows Installer Dokumentation.<br/>       |
| [Übersicht](about-windows-installer.md)<br/>                                          | Allgemeine Informationen zum Installationsprogramm.<br/>          |
| [Neues in Windows Installer](what-s-new-in-windows-installer.md)<br/>           | Listet Ergänzungen und Änderungen an der Windows Installer auf.<br/> |
| [Verweis](installer-function-reference.md)<br/>                                    | Dokumentation zu Windows Installer Funktionen.<br/>     |
| [Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)<br/> | Windows Installer Beispiele mit Skripts.<br/>          |



 

 

 
