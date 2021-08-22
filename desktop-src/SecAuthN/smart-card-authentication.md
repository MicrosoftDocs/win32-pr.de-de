---
description: Smartcard-Authentifizierung
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Smartcard-Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bccfa9e762c137e332c26b5375584658c22718d336800b6dc73cf056ebde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918006"
---
# <a name="smart-card-authentication"></a>Smartcard-Authentifizierung

Die grundlegenden Teile des [*Smartcard-Subsystems*](../secgloss/s-gly.md) basieren auf PC/SC-Standards (siehe Spezifikationen unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Zu diesen grundlegenden Teilen gehören:

-   Ein [*Ressourcen-Manager,*](../secgloss/r-gly.md) der eine Windows-API verwendet.
-   Eine [*Benutzeroberfläche,*](../secgloss/u-gly.md) die mit dem Ressourcen-Manager funktioniert.
-   Mehrere [*Basisdienstanbieter,*](../secgloss/s-gly.md) die Zugriff auf bestimmte Dienste bereitstellen. Im Gegensatz zur Windows-API des Ressourcen-Managers verwenden Dienstanbieter ein COM-Schnittstellenmodell, um [*Smartcarddienste*](../secgloss/s-gly.md) bereitzustellen.

Die folgende Abbildung zeigt die Beziehungen dieser Teile in der gesamten Smartcardarchitektur.

![Smartcardarchitektur](images/smartovr2a.png)

Informationen zur Funktionsweise des [*Smartcardsubsystems*](../secgloss/s-gly.md) mit anderen Diensten, die im Microsoft Internet Security Framework verfügbar sind, finden Sie unter [Beziehung zu anderen Diensten.](relation-to-other-services.md)

Informationen zur Smartcard-Authentifizierung finden Sie in den folgenden Themen.



| Themen                                                                      | Inhalte                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Smartcardkonzepte](smart-card-concepts.md)<br/>                   | Grundlegende Konzepte und Beschreibung der Interaktion zwischen Benutzern und Smartcards.<br/>                                                                                                                                                        |
| [Smartcard-Resource Manager](smart-card-resource-manager.md)<br/>   | Informationen zur Resource Manager-API, die den Zugriff auf [*Leser*](../secgloss/r-gly.md) und [*Smartcards*](../secgloss/s-gly.md)verwaltet.<br/> |
| [Smartcard-Benutzeroberfläche](smart-card-user-interface.md)<br/>       | Informationen zum [*allgemeinen Smartcarddialogfeld*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Smartcard-Dienstanbieter](smart-card-service-providers.md)<br/> | Informationen zu Schnittstellen, Befehlen und Wrappern, die Smartcardfunktionen bereitstellen.<br/>                                                                                                                                              |



 

Darüber hinaus finden Sie die aktuellen Entwicklungen bei Microsoft-Smartcards unter [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
