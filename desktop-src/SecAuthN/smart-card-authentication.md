---
description: Smartcardauthentifizierung
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Smartcardauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350026"
---
# <a name="smart-card-authentication"></a>Smartcardauthentifizierung

Die grundlegenden Teile des [*Smartcard-Subsystems*](../secgloss/s-gly.md) basieren auf PCs/SC-Standards (siehe Spezifikationen unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Diese grundlegenden Teile umfassen Folgendes:

-   Ein [*Ressourcen-Manager*](../secgloss/r-gly.md) , der eine Windows-API verwendet.
-   Eine [*Benutzeroberfläche*](../secgloss/u-gly.md) (UI), die mit dem Ressourcen-Manager verwendet werden kann.
-   Mehrere Basis [*Dienstanbieter*](../secgloss/s-gly.md) , die Zugriff auf bestimmte Dienste ermöglichen. Im Gegensatz zur Windows-API des Ressourcen-Managers verwenden Dienstanbieter ein COM-Schnittstellen Modell, um [*smartcarddienste*](../secgloss/s-gly.md) bereitzustellen.

Die folgende Abbildung zeigt die Beziehungen dieser Teile in der gesamten smartcardarchitektur.

![smartcardarchitektur](images/smartovr2a.png)

Informationen dazu, wie das [*Smartcard-Subsystem*](../secgloss/s-gly.md) mit anderen im Microsoft Internet Security Framework verfügbaren Diensten funktioniert, finden [Sie unter Relation zu anderen Diensten](relation-to-other-services.md).

Informationen zur Smartcardauthentifizierung finden Sie in den folgenden Themen.



| Themen                                                                      | Inhalte                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Smartcardkonzepte](smart-card-concepts.md)<br/>                   | Grundlegende Konzepte und Beschreibungen der Interaktion zwischen Benutzern und Smartcards.<br/>                                                                                                                                                        |
| [Smartcard-Ressourcen-Manager](smart-card-resource-manager.md)<br/>   | Informationen zur Resource Manager-API, die den Zugriff auf [*Leser*](../secgloss/r-gly.md) und [*Smartcards*](../secgloss/s-gly.md)verwaltet.<br/> |
| [Smartcard-Benutzeroberfläche](smart-card-user-interface.md)<br/>       | Informationen zum [*Dialogfeld "Smartcard-allgemein*](../secgloss/s-gly.md)".<br/>                                                                                   |
| [Smartcarddienstanbieter](smart-card-service-providers.md)<br/> | Informationen zu Schnittstellen, Befehlen und Wrappern, die Smartcardfunktionen bereitstellen.<br/>                                                                                                                                              |



 

Darüber hinaus finden Sie aktuelle Microsoft-smartcardentwicklungen unter [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
