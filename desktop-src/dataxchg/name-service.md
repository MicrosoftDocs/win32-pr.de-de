---
title: Namensdienst
description: In diesem Thema wird erläutert, wie die dynamischer Datenaustausch-Verwaltungs Bibliothek es einer Serveranwendung ermöglicht, die von ihr unterstützten Dienstnamen zu registrieren.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Namensdienst
- DDE (dynamischer Datenaustausch), Namensdienst
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Name Service
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Namensdienst
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch (DDE), Dienstnamen Registrierung
- DDE (dynamischer Datenaustausch), Dienstnamen Registrierung
- Dynamischer Datenaustausch Management Library (Ddeml), Dienstnamen Registrierung
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Dienstnamen Registrierung
- Dynamischer Datenaustausch (DDE), Dienst namens Filter
- DDE (dynamischer Datenaustausch), Dienst namens Filter
- Dynamischer Datenaustausch Management Library (Ddeml), Dienst namens Filter
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Dienst namens Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311501"
---
# <a name="name-service"></a>Namensdienst

Die dynamischer Datenaustausch Management Library (Ddeml) ermöglicht es einer Serveranwendung, die von ihr unterstützten Dienstnamen zu registrieren und zu verhindern, dass die Ddeml [**XYP \_ Connect**](xtyp-connect.md) -Transaktionen für nicht unterstützte Dienstnamen an die dynamischer Datenaustausch (DDE)-Rückruffunktion des Servers sendet.

In den folgenden Themen wird der Name Service beschrieben.

-   [Dienstnamen Registrierung](#service-name-registration)
-   [Dienst namens Filter](#service-name-filter)

## <a name="service-name-registration"></a>Dienstnamen Registrierung

Wenn die Dienstnamen bei der Ddeml registriert werden, informiert ein Server andere DDE-Anwendungen im System, dass ein neuer Server verfügbar ist. Ein Server registriert einen Dienstnamen durch Aufrufen der Funktion " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " und durch Angabe eines Zeichen folgen Handles, das den Namen identifiziert. In der Antwort sendet die Ddeml eine [**xtipp- \_ Register**](xtyp-register.md) Transaktion an die Rückruffunktion der einzelnen Ddeml-Anwendungen im System (mit Ausnahme derjenigen, die das CBF \_ Skip \_ registrierungsfilterflag in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben haben). Die **xtipp- \_ Registrierungs** Transaktion übergibt zwei Zeichen folgen Handles an eine Rückruffunktion: die erste identifiziert die Zeichenfolge, die den Basis Dienstnamen angibt, und die zweite identifiziert die Zeichenfolge, die den instanzspezifischen Dienst angibt. Ein Client verwendet in der Regel den Basis Dienstnamen in einer Liste verfügbarer Server, sodass der Benutzer einen Server aus der Liste auswählen kann. Der Client verwendet den instanzspezifischen Dienstnamen, um eine Konversation mit einer bestimmten Instanz einer Serveranwendung herzustellen, wenn mehr als eine Instanz ausgeführt wird.

Ein Server kann mit [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) die Registrierung eines Dienst namens aufheben. Diese Funktion bewirkt, dass die Ddeml [**XYP- \_ Unregister**](xtyp-unregister.md) -Transaktionen an die anderen DDE-Anwendungen im System sendet und Sie darüber informiert, dass Sie den Namen nicht mehr zum Einrichten von Konversationen verwenden können.

Ein Server muss " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " aufrufen, um die Dienstnamen kurz nach dem Aufrufen von " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)" zu registrieren. Ein Server muss die Registrierung seiner Dienstnamen mithilfe von **DDENameService** unmittelbar vor dem Aufrufen der [**ddeuninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) -Funktion aufheben.

## <a name="service-name-filter"></a>Dienst namens Filter

Neben dem Registrieren von Dienstnamen ermöglicht [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) einem Server, seinen Dienst namens Filter ein-oder auszuschalten. Wenn ein Server den Dienst namens Filter deaktiviert, sendet die Ddeml die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion an die DDE-Rückruffunktion des Servers, wenn ein Client die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -Funktion aufruft, unabhängig von dem in der Funktion angegebenen Dienstnamen. Wenn ein Server seinen Dienstnamen Filter aufruft, sendet die Ddeml die **xtipp \_ Connect** -Transaktion nur an den Server, wenn **ddeconnect** einen Dienstnamen angibt, den der Server bei einem " **DDENameService**"-Befehl angegeben hat.

Standardmäßig ist der Dienst namens Filter aktiviert, wenn eine Anwendung [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)aufruft. Mit dieser Standardeinstellung wird verhindert, dass die Ddeml die [**XYP \_ Connect**](xtyp-connect.md) -Transaktion an einen Server sendet, bevor der Server die benötigten Zeichen folgen Handles erstellt hat. Ein Server kann seinen Dienst namens Filter deaktivieren, indem er das DNS- \_ filteroff-Flag in einem Befehl an " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)" angibt. Das DNS- \_ FilterOn-Flag schaltet den Filter ein.

 

 




