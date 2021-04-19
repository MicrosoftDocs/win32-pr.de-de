---
description: Das Windows-Sicherheitsmodell ermöglicht es Aufrufern von Kerneltransaktions-Manager (KTM), den Zugriff auf Transaktionen, den Transaktions-Manager, den Ressourcen-Manager und die Eintragung zu steuern.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Sicherheit und Zugriffsrechte für KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349633"
---
# <a name="ktm-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für KTM

Das Windows-Sicherheitsmodell ermöglicht es Aufrufern von Kerneltransaktions-Manager (KTM), den Zugriff auf Transaktionen, den Transaktions-Manager, den Ressourcen-Manager und die Eintragung zu steuern. Weitere Informationen finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model). Für Anwendungen, die sich nicht auf die Sicherheit beziehen, können Transaktionen mit Zuordnungs Zugriffs Steuerungs Listen (ACLs) erstellt werden, mit denen sich alle Ressourcen-Manager in einer Transaktion eintragen lassen können.

## <a name="transactions"></a>Transaktionen

Wenn ein Client die [**opentransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) -Funktion verwendet, überprüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Transaktions Objekts.

Zu den gültigen Zugriffsrechten für Transaktions Objekte zählen die Möglichkeit, Informationen abzufragen und festzulegen sowie Informationen, eintragen und verschiedene Transaktions Vorgänge sowie [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)zu erhalten. [**Transaktions Zugriffs Masken**](transaction-access-masks.md) listet die spezifischen Zugriffsrechte für eine Transaktion auf.

Da Transaktionen einen permanenten Status aufweisen, ist es wichtig, dass RMS und TMS, die mit KTM interagieren, ihre Verpflichtungen hinsichtlich der Wiederherstellung erfüllen. Wenn diese Verpflichtungen nicht erfüllt werden, kann dies zu Ressourcenverlusten führen, die selbst bei einem Systemneustart nicht bereinigt werden. Beachten Sie die Auswirkung eines permanenten oder bösartigen Codes, der dazu geführt hat, dass der KTM Kernel Ressourcen verbraucht hat, bis ein Systemfehler aufgetreten ist. nach dem resultierenden Neustart würde der KTM sein Protokoll lesen und alle persistenten Objekte neu erstellen, wodurch möglicherweise der gleiche Systemfehler wiederholt wird. Bei der Kontingent basierten Drosselung wird eine persistente Ressourcen Hungersnot durch eine nicht autorisierte oder nicht verhaltende RM verhindert. Schließlich müssen administrative Mechanismen erstellt werden, die die Erkennung und Korrektur solcher persistente Verluste ermöglichen.

## <a name="transaction-managers"></a>Transaktions-Manager

Wenn ein Client die [**opentransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) -Funktion verwendet, überprüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Resource Manager-Objekts.

Zu den gültigen Zugriffsrechten für Transaktions-Manager-Objekte zählen die Möglichkeit, Informationen abzufragen und festzulegen, RMS zu erstellen, Vorgänge zu erstellen und umzubenennen sowie [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights). In den [**Zugriffs Masken des Transaktions-Managers**](transaction-manager-access-masks.md) sind die spezifischen Zugriffsrechte für einen Transaktions-Manager aufgeführt.

Ein Ressourcen-Manager kann eigene Transaktions-Manager-Objekte mit restriktiven ACLs erstellen, um einzuschränken, welche Ressourcen-Manager an Transaktionen teilnehmen können, die das Protokoll dieses Transaktions-Managers verwenden.

## <a name="resource-managers"></a>Ressourcen-Manager

Wenn ein Client die [**openresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) -Funktion verwendet, überprüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Resource Manager-Objekts.

Zu den gültigen Zugriffsrechten für Resource Manager-Objekte zählen die Möglichkeit, Informationen abzufragen und festzulegen, wiederherzustellen, zu registrieren, Registrierungs Vorgänge sowie Weiterleitungs-und Wiederherstellungs Vorgänge sowie [Standardrechte zu ermöglichen](/windows/desktop/SecAuthZ/standard-access-rights). [**Ressourcen-Manager Zugriffs Masken**](resource-manager-access-masks.md) listet die spezifischen Zugriffsrechte für einen Ressourcen-Manager auf.

Ein Ressourcen-Manager kann seine eigenen Resource Manager-Objekte mit restriktiven Zugriffs Steuerungs Listen erstellen, wenn er verhindert, dass böswillige Code Benachrichtigungen abfängt oder bestimmte Transaktionsergebnisse erzwingt.

## <a name="enlistments"></a>Eintragungen

Wenn ein Client die [**openenlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) -Funktion verwendet, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung für das Eintragung-Objekt.

Zu den gültigen Zugriffsrechten für die Eintragung von Objekten zählen die Möglichkeit, Informationen abzufragen und festzulegen sowie Wiederherstellungs Vorgänge sowie [Standardrechte zu ermöglichen](/windows/desktop/SecAuthZ/standard-access-rights). Die [**Zugriffs Masken der Eintragung**](enlistment-access-masks.md) listet die spezifischen Zugriffsrechte für eine Eintragung auf.

 

 
