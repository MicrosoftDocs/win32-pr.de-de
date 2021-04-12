---
description: Mit der Authz-API können Anwendungen anpassbare Zugriffs Überprüfungen durchführen, um die Leistung zu verbessern und die Access Control Entwicklung zu vereinfachen.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Verwenden der Authz-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349708"
---
# <a name="using-authz-api"></a>Verwenden der Authz-API

Mit der Authz-API können Anwendungen anpassbare Zugriffs Überprüfungen durchführen, um die Leistung zu verbessern und die [Access Control](low-level-access-control.md)Entwicklung zu vereinfachen.

Mit der Authz-API können Anwendungen Zugriffs Überprüfungen Zwischenspeichern, um die Leistung zu verbessern, Client Kontexte abzufragen und zu ändern und Geschäftsregeln zu definieren, die zum dynamischen Auswerten der Zugriffsberechtigung verwendet werden können.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Initialisieren eines Client Kontexts](initializing-a-client-context.md)<br/>     | Eine Anwendung muss einen Client Kontext erstellen, bevor Sie mit der Authz-API Zugriffs Überprüfungen oder-Überwachungen durchführen kann.<br/>                                                                                                                                            |
| [Abfragen eines Client Kontexts](querying-a-client-context.md)<br/>             | Anwendungen können die [**AuthZGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) -Funktion aufrufen, um Informationen über einen vorhandenen Client Kontext abzufragen.<br/>                                                                                       |
| [Hinzufügen von SIDs zu einem Client Kontext](adding-sids-to-a-client-context.md)<br/> | Eine Anwendung kann einem vorhandenen Client Kontext [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) hinzufügen, indem Sie die [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) -Funktion aufrufen.<br/> |
| [Überprüfen des Zugriffs mit der Authz-API](checking-access-with-authz-api.md)<br/>   | Anwendungen bestimmen, ob der Zugriff auf Sicherungs fähige Objekte durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion gewährt werden soll.<br/>                                                                                                                |
| [Caching-Zugriffs Überprüfungen](caching-access-checks.md)<br/>                     | Wenn eine Anwendung eine Zugriffs Überprüfung durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion durchführt, können die Ergebnisse dieser Zugriffs Überprüfung zwischengespeichert werden.<br/>                                                                                       |



 

 

