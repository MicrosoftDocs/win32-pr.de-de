---
description: Ein Konfigurationsprogramm verwendet die Funktion "| ateservice", um einen neuen Dienst in der SCM-Datenbank zu installieren.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Dienst Installation, Entfernung und Enumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751057"
---
# <a name="service-installation-removal-and-enumeration"></a>Dienst Installation, Entfernung und Enumeration

Ein Konfigurationsprogramm verwendet die Funktion "| [**ateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ", um einen neuen Dienst in der SCM-Datenbank zu installieren. Diese Funktion gibt den Namen des Dienstanbieter an und stellt Konfigurationsinformationen bereit, die in der Datenbank gespeichert sind. Eine Beschreibung der Informationen, die in der Datenbank für die einzelnen Dienste gespeichert sind, finden Sie unter [Datenbank der installierten Dienste](database-of-installed-services.md). Beispielcode finden Sie unter [Installieren eines Dienstanbieter](installing-a-service.md).

Ein Konfigurationsprogramm verwendet die Funktion " [**Delta**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) Service", um einen installierten Dienst aus der Datenbank zu entfernen. Weitere Informationen finden Sie unter [Löschen eines Dienstanbieter](deleting-a-service.md).

Um den Dienstnamen zu erhalten, rufen Sie die [**getservicekeyname**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) -Funktion auf. Der Anzeige Name des Diensts, der in der System Steuerungs Option "Dienste" verwendet wird, kann durch Aufrufen der Funktion " [**getservicedisplayname**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) " abgerufen werden.

Ein Dienst Konfigurationsprogramm kann die [**EnumServicesStatus usex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) -Funktion verwenden, um alle Dienste und deren Status aufzulisten. Sie kann auch die [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) -Funktion verwenden, um aufzulisten, welche Dienste von einem angegebenen Dienst Objekt abhängig sind.

 

 



