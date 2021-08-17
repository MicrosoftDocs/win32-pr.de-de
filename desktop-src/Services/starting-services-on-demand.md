---
description: Der Benutzer kann einen Dienst mit dem Systemsteuerungs-Hilfsprogramm Dienste starten. Der Benutzer kann Argumente für den Dienst im Feld Startparameter angeben. Ein Dienststeuerungsprogramm kann einen Dienst starten und seine Argumente mit der StartService-Funktion angeben.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Starten von Diensten bei Bedarf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3762721eaeaea32d42da729f57c0753b18fb951cb57ad091aa697c144df0de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888466"
---
# <a name="starting-services-on-demand"></a>Starten von Diensten bei Bedarf

Der Benutzer kann einen Dienst mit dem Systemsteuerungs-Hilfsprogramm Dienste starten. Der Benutzer kann Argumente für den Dienst im Feld **Startparameter** angeben. Ein Dienststeuerungsprogramm kann einen Dienst starten und seine Argumente mit der [**StartService-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) angeben.

Wenn der Dienst gestartet wird, führt der SCM die folgenden Schritte aus:

-   Rufen Sie die in der Datenbank gespeicherten Kontoinformationen ab.
-   Melden Sie sich beim Dienstkonto an.
-   Laden Sie das Benutzerprofil.
-   Erstellen Sie den Dienst im Angehalten-Zustand.
-   Weisen Sie das Anmeldetoken dem Prozess zu.
-   Lassen Sie die Ausführung des Prozesses zu.

 

 



