---
description: Mit dem Windows-Sicherheitsmodell können Aufrufer von Kernel Transaction Manager (CSV) den Zugriff auf Transaktions-, Transaktions-Manager-, Ressourcen-Manager- und Eintragungsobjekte steuern.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: SECURITY and Access Rights (SICHERHEITS- und Zugriffsrechte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0baf273b45a886e40c731c44c261f836fdc0b79012f906a1b4adfe07083be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388892"
---
# <a name="ktm-security-and-access-rights"></a>SECURITY and Access Rights (SICHERHEITS- und Zugriffsrechte)

Mit dem Windows-Sicherheitsmodell können Aufrufer von Kernel Transaction Manager (CSV) den Zugriff auf Transaktions-, Transaktions-Manager-, Ressourcen-Manager- und Eintragungsobjekte steuern. Weitere Informationen finden Sie unter [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model). Für Anwendungen, die sich nicht um die Sicherheit kümmern, können Transaktionen mit zugriffssteuerungslisten (ACLs) erstellt werden, die es jedem Ressourcen-Manager ermöglichen, sich für eine Transaktion zu eintragen.

## <a name="transactions"></a>Transaktionen

Wenn ein Client die [**OpenTransaction-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) verwendet, überprüft das System die angeforderten Zugriffsrechte anhand des Sicherheitsdeskriptors für das Transaktionsobjekt.

Zu den gültigen Zugriffsrechten für Transaktionsobjekte gehören die Möglichkeit zum Abfragen und Festlegen von Informationen, zum Eintragen und zu verschiedenen Transaktionsvorgängen sowie zu [Standardzugriffsrechten.](/windows/desktop/SecAuthZ/standard-access-rights) [**Transaktionszugriffsmasken**](transaction-access-masks.md) listen die spezifischen Zugriffsrechte für eine Transaktion auf.

Da Transaktionen einen dauerhaften Zustand aufweisen, ist es von entscheidender Bedeutung, dass RMs und TMs, die mit der MSI interagieren, ihre Verpflichtungen in Bezug auf die Wiederherstellung erfüllen. Wenn diese Verpflichtungen nicht erfüllt werden, kann dies zu Ressourcenverlusten führen, die selbst bei einem Systemneustart nicht bereinigt werden. Berücksichtigen Sie die Auswirkungen eines dauerhaften Verlusts oder schädlichen Codes, der dazu geführt hat, dass die KERNEL-Ressourcen von DER ZEIT bis zu einem Systemfehler verbraucht wurden. Nach dem daraus resultierenden Neustart liest die PROTOKOLLDATEI das Protokoll und erstellt alle persistenten Objekte neu, was möglicherweise dazu führt, dass derselbe Systemfehler erneut auftritt. Durch eine kontingentbasierte Drosselung wird verhindert, dass ein nicht autorisierter oder falscher RM dauerhaft ressourcenverhungern kann. Schließlich müssen Verwaltungsmechanismen erstellt werden, die die Erkennung und Korrektur solcher dauerhaften Lecks ermöglichen.

## <a name="transaction-managers"></a>Transaktions-Manager

Wenn ein Client die [**OpenTransactionManager-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) verwendet, überprüft das System die angeforderten Zugriffsrechte anhand des Sicherheitsdeskriptors für das Resource Manager-Objekt.

Die gültigen Zugriffsrechte für Transaktions-Manager-Objekte umfassen die Möglichkeit, Informationen abzufragen und festzulegen, RMs zu erstellen und Vorgänge wiederherzustellen und umzubenennen, sowie [Standardzugriffsrechte.](/windows/desktop/SecAuthZ/standard-access-rights) [**Transaktions-Manager-Zugriffsmasken listet**](transaction-manager-access-masks.md) die spezifischen Zugriffsrechte für einen Transaktions-Manager auf.

Ein Ressourcen-Manager kann eigene Transaktions-Manager-Objekte mit restriktiven ACLs erstellen, um einzuschränken, welche Ressourcen-Manager an Transaktionen teilnehmen können, die das Protokoll dieses Transaktions-Managers verwenden.

## <a name="resource-managers"></a>Ressourcen-Manager

Wenn ein Client die [**OpenResourceManager-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) verwendet, überprüft das System die angeforderten Zugriffsrechte anhand des Sicherheitsdeskriptors für das Resource Manager-Objekt.

Zu den gültigen Zugriffsrechten für Resource Manager-Objekte gehören die Möglichkeit, Informationen abzufragen und festzulegen, Wiederherstellungs-, Eintragungs-, Registrierungs- und Weitergabe- und Wiederherstellungsvorgänge sowie [Standardzugriffsrechte.](/windows/desktop/SecAuthZ/standard-access-rights) [**Resource Manager Access Masks listet**](resource-manager-access-masks.md) die spezifischen Zugriffsrechte für einen Ressourcen-Manager auf.

Ein Ressourcen-Manager kann eigene Resource Manager-Objekte mit restriktiven ACLs erstellen, wenn er verhindern möchte, dass schädlicher Code Benachrichtigungen abfängt oder bestimmte Transaktionsergebnisse erzwingt.

## <a name="enlistments"></a>Eintragungen

Wenn ein Client die [**OpenEnlistment-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) verwendet, überprüft das System die angeforderten Zugriffsrechte anhand des Sicherheitsdeskriptors für das Eintragungsobjekt.

Die gültigen Zugriffsrechte für Eintragungsobjekte umfassen die Möglichkeit, Informationen abzufragen und festzulegen, Wiederherstellungsvorgänge durchzuführen, sowie [Standardzugriffsrechte.](/windows/desktop/SecAuthZ/standard-access-rights) [**Unter Eintragszugriffsmasken**](enlistment-access-masks.md) werden die spezifischen Zugriffsrechte für eine Eintragung aufgeführt.

 

 
