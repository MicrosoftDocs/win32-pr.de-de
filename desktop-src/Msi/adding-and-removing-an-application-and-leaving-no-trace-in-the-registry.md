---
description: Wenn eine Anwendung registriert werden muss, erstellen Sie das Installationspaket, wie im Abschnitt hinzufügen und Entfernen von Registrierungs Schlüsseln zum Installieren oder Entfernen von-Komponenten beschrieben.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Hinzufügen und Entfernen einer Anwendung ohne Ablauf Verfolgung in der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36804633a51e0e2f4beafc37e9f830e1743a5ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959547"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Hinzufügen und Entfernen einer Anwendung ohne Ablauf Verfolgung in der Registrierung

Wenn eine Anwendung registriert werden muss, erstellen Sie das Installationspaket, wie im Abschnitt [Hinzufügen und Entfernen von Registrierungs Schlüsseln zum Installieren oder Entfernen von-Komponenten](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)beschrieben. Die Registrierung wird vom Installationsprogramm für die Ankündigung und durch die Funktion "Software" in der Systemsteuerung verwendet. Wenn eine Anwendung nicht registriert ist, kann Sie nicht angekündigt werden und ist in der Systemsteuerung nicht in der Funktion "Software" aufgeführt.

Sie können die Registrierung einer Anwendung weglassen, indem Sie die Aktion [registerproduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [publishproduct Action](publishproduct-action.md)und [publishfeatures](publishfeatures-action.md) aus der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) und der [AdvtExecuteSequence](advtexecutesequence-table.md)-Tabelle entfernen. Alle diese Aktionen müssen entfernt werden, oder es kann eine Ablauf Verfolgung der Anwendung in der Registrierung verbleiben. Wenn Sie alle diese Aktionen entfernen, wird verhindert, dass die Anwendung in der Systemsteuerung in der Funktion "Software" aufgeführt wird, und die Ankündigung der Anwendung wird verhindert. Durch das Entfernen all dieser Aktionen wird auch verhindert, dass die Anwendung mit den Windows Installer Konfigurationsdaten registriert wird. Dies bedeutet, dass Sie die Anwendung nicht mithilfe der Windows Installer [Befehlszeilenoptionen](command-line-options.md)oder der Windows Installer Application Programming Interface (API) entfernen, reparieren oder neu installieren können.

Wenn Sie eine Anwendung in der Systemsteuerung über das Feature "Software" ausblenden möchten und die Windows Installer weiterhin zum Verwalten einer Anwendung verwenden können, belassen Sie die Registrierungsaktionen in den Sequenz Tabellen, und legen Sie die [**Eigenschaft "ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) " in der [Eigenschaften Tabelle](property-table.md) auf 1 (eins) fest. Die Anwendung wird nicht im Feature zum Hinzufügen oder Entfernen von Software angezeigt, Sie können jedoch die Windows Installer verwenden, um die Anwendung bei Bedarf zu installieren, zu deinstallieren, zu reparieren und erneut zu installieren.

 

 



