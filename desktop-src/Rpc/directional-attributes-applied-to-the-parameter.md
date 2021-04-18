---
title: Auf den Parameter angewendete direktionale Attribute
description: Die direktionalen Attribute \ in \ und \ out \ bestimmen, wie der Client und der Server Arbeitsspeicher zuordnen und freigeben. In der folgenden Tabelle werden die Auswirkungen der direktionalen Attribute auf die Speicher Belegung zusammengefasst.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340929"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Auf den Parameter angewendete direktionale Attribute

Die direktionalen Attribute \[ [in](/windows/desktop/Midl/in) \] und \[ [out](/windows/desktop/Midl/out-idl) \] bestimmen, wie der Client und der Server Arbeitsspeicher zuordnen und freigeben. In der folgenden Tabelle werden die Auswirkungen der direktionalen Attribute auf die Speicher Belegung zusammengefasst.



| Direktionales Attribut    | Arbeitsspeicher auf dem Client                                                                                            | Arbeitsspeicher auf dem Server                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[in](/windows/desktop/Midl/in)\]       | Die Client Anwendung muss vor dem-Befehl zuordnen.                                                           | Server-Stub zugeordnet.                                                                                                                                  |
| \[[out](/windows/desktop/Midl/out-idl)\] | Der Clientstub ordnet bei der Rückgabe zu.                                                                            | Der Serverstub weist nur Zeiger der obersten Ebene zu. die Serveranwendung muss alle eingebetteten Zeiger zuordnen. Der Server ordnet bei Bedarf auch neue Daten zu. |
| \[**in**, **out**\]      | Die Client Anwendung muss die dem Server übertragenen anfänglichen Daten zuordnen. der Clientstub ordnet zusätzliche Daten zu. | Der Serverstub ordnet anfängliche Daten zu, die vom Client gesendet werden. die Serveranwendung ordnet bei Bedarf neue Daten zu.                                        |



 

In all diesen Fällen gibt der Clientstub keinen Arbeitsspeicher frei. Die Client Anwendung muss den Arbeitsspeicher freigeben, bevor Sie beendet wird. Der Serverstub gibt Arbeitsspeicher frei, wenn der Remote Prozedur Rückruf zurückkehrt (unterliegt dem \[ [](/windows/desktop/Midl/allocate) \] ACF-Attribut "zuordnen").

 

 