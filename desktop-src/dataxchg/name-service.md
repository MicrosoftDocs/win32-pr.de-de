---
title: Name Service
description: In diesem Thema wird erläutert, wie die dynamische Daten Exchange-Verwaltungsbibliothek es einer Serveranwendung ermöglicht, die unterstützten Dienstnamen zu registrieren.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE),Name-Dienst
- DDE (dynamische Daten Exchange),Name-Dienst
- Datenaustausch, dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML),Name-Dienst
- DDEML (dynamische Daten Exchange Management Library),Name-Dienst
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange (DDE),Dienstnamenregistrierung
- DDE (dynamische Daten Exchange),Dienstnamenregistrierung
- dynamische Daten Exchange Management Library (DDEML), Dienstnamenregistrierung
- DDEML (dynamische Daten Exchange Management Library),Dienstnamenregistrierung
- dynamische Daten Exchange (DDE), Dienstnamenfilter
- DDE (dynamische Daten Exchange),Dienstnamenfilter
- dynamische Daten Exchange Management Library (DDEML), Dienstnamenfilter
- DDEML (dynamische Daten Exchange Management Library),Dienstnamenfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7346bd98979e9bd5a4aa0e43493e975d802875cf8fd0fc79d7bd002bcd0c5494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811647"
---
# <a name="name-service"></a>Name Service

Die dynamische Daten Exchange Management Library (DDEML) ermöglicht es einer Serveranwendung, die unterstützten Dienstnamen zu registrieren und zu verhindern, dass die DDEML [**XTYP \_ CONNECT-Transaktionen**](xtyp-connect.md) für nicht unterstützte Dienstnamen an die Rückruffunktion dynamische Daten Exchange (DDE) des Servers sendet.

In den folgenden Themen wird der Namensdienst beschrieben.

-   [Dienstnamenregistrierung](#service-name-registration)
-   [Dienstnamenfilter](#service-name-filter)

## <a name="service-name-registration"></a>Dienstnamenregistrierung

Durch die Registrierung seiner Dienstnamen bei der DDEML informiert ein Server andere DDE-Anwendungen im System darüber, dass ein neuer Server verfügbar ist. Ein Server registriert einen Dienstnamen, indem er die [**DdeNameService-Funktion aufruft**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) und ein Zeichenfolgenhandle angibt, das den Namen identifiziert. Als Reaktion sendet die DDEML eine [**XTYP \_ REGISTER-Transaktion**](xtyp-register.md) an die Rückruffunktion jeder DDEML-Anwendung im System (mit Ausnahme derjenigen, die das CBF \_ SKIP \_ REGISTRATIONS-Filterflag in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angegeben haben). Die **XTYP \_ REGISTER-Transaktion** übergibt zwei Zeichenfolgenhandles an eine Rückruffunktion: der erste identifiziert die Zeichenfolge, die den Basisdienstnamen angibt, und der zweite gibt die Zeichenfolge an, die den instanzspezifischen Dienst angibt. Ein Client verwendet in der Regel den Basisdienstnamen in einer Liste verfügbarer Server, sodass der Benutzer einen Server aus der Liste auswählen kann. Der Client verwendet den instanzspezifischen Dienstnamen, um eine Konversation mit einer bestimmten Instanz einer Serveranwendung herzustellen, wenn mehrere Instanzen ausgeführt werden.

Ein Server kann [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) verwenden, um die Registrierung eines Dienstnamens zu aufheben. Diese Funktion bewirkt, dass die DDEML [**XTYP \_ UNREGISTER-Transaktionen**](xtyp-unregister.md) an die anderen DDE-Anwendungen im System sendet und sie darüber informiert, dass sie den Namen nicht mehr zum Einrichten von Konversationen verwenden können.

Ein Server muss [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) aufrufen, um seine Dienstnamen kurz nach dem Aufruf von [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)zu registrieren. Ein Server muss die Registrierung seiner Dienstnamen mithilfe von **DdeNameService** aufheben, bevor er die [**DdeUninitialize-Funktion aufruft.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)

## <a name="service-name-filter"></a>Dienstnamenfilter

Zusätzlich zum Registrieren von Dienstnamen ermöglicht [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) einem Server, seinen Dienstnamenfilter zu aktivieren oder zu deaktivieren. Wenn ein Server seinen Dienstnamenfilter deaktiviert, sendet die DDEML die [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) an die DDE-Rückruffunktion des Servers, wenn ein Client die [**DdeConnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) aufruft, unabhängig vom in der Funktion angegebenen Dienstnamen. Wenn ein Server seinen Dienstnamenfilter aktiviert, sendet die DDEML die **XTYP \_ CONNECT-Transaktion** nur dann an den Server, wenn **DdeConnect** einen Dienstnamen angibt, den der Server in einem Aufruf von **DdeNameService** angegeben hat.

Standardmäßig ist der Dienstnamenfilter aktiviert, wenn eine Anwendung [**DdeInitialize aufruft.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Dieser Standardwert verhindert, dass die DDEML die [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) an einen Server sendet, bevor der Server die benötigten Zeichenfolgenhandles erstellt hat. Ein Server kann seinen Dienstnamenfilter deaktivieren, indem er \_ das DNS-FILTEROFF-Flag in einem Aufruf von [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)angibt. Das DNS \_ FILTERON-Flag aktiviert den Filter.

 

 




