---
description: Der Benutzer kann einen Dienst mit dem Dienststeuerungs-Hilfsprogramm "Dienste" starten. Der Benutzer kann Argumente für den Dienst im Feld Start Parameter angeben. Ein Dienst Steuerungsprogramm kann einen Dienst starten und seine Argumente mit der Start Service-Funktion angeben.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Starten von Diensten bei Bedarf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351513"
---
# <a name="starting-services-on-demand"></a>Starten von Diensten bei Bedarf

Der Benutzer kann einen Dienst mit dem Dienststeuerungs-Hilfsprogramm "Dienste" starten. Der Benutzer kann Argumente für den Dienst im Feld **Start Parameter** angeben. Ein Dienst Steuerungsprogramm kann einen Dienst starten und seine Argumente mit der [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) -Funktion angeben.

Wenn der Dienst gestartet wird, führt der SCM die folgenden Schritte aus:

-   Ruft die in der-Datenbank gespeicherten Kontoinformationen ab.
-   Melden Sie sich mit dem Dienst Konto an.
-   Laden Sie das Benutzerprofil.
-   Erstellen Sie den Dienst im Zustand "angehalten".
-   Weisen Sie das Anmelde Token dem Prozess zu.
-   Ermöglicht die Ausführung des Prozesses.

 

 



