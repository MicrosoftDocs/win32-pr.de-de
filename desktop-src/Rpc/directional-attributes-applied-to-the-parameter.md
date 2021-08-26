---
title: Auf den Parameter angewendete direktionale Attribute
description: Die direktionalen Attribute \ in\ und \ out\ bestimmen, wie der Client und der Server Arbeitsspeicher zuordnen und freigeben. In der folgenden Tabelle werden die Auswirkungen von richtungsdirektionalen Attributen auf die Speicherbelegung zusammengefasst.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e18e34a7ea553fd5c1fd9157877a0296e403443fc490bb328f48ac4b7b2c8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073390"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Auf den Parameter angewendete direktionale Attribute

Die direktionalen Attribute \[ [in](/windows/desktop/Midl/in) \] und \[ [out](/windows/desktop/Midl/out-idl) \] bestimmen, wie der Client und der Server Arbeitsspeicher zuordnen und freigeben. In der folgenden Tabelle werden die Auswirkungen von richtungsdirektionalen Attributen auf die Speicherbelegung zusammengefasst.



| Direktionales Attribut    | Arbeitsspeicher auf dem Client                                                                                            | Arbeitsspeicher auf dem Server                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[in](/windows/desktop/Midl/in)\]       | Die Clientanwendung muss vor dem Aufruf zuordnen.                                                           | Serverstub belegt.                                                                                                                                  |
| \[[out](/windows/desktop/Midl/out-idl)\] | Clientstub ordnet bei Rückgabe zu.                                                                            | Der Serverstub weist nur Zeiger der obersten Ebene zu. Die Serveranwendung muss alle eingebetteten Zeiger zuordnen. Der Server ordnet bei Bedarf auch neue Daten zu. |
| \[**in**, **out**\]      | Die Clientanwendung muss anfänglich an den Server übertragene Daten zuordnen. Der Clientstub ordnet zusätzliche Daten zu. | Der Serverstub ordnet die anfänglich vom Client übertragenen Daten zu. Die Serveranwendung ordnet nach Bedarf neue Daten zu.                                        |



 

In all diesen Fällen gibt der Clientstub keinen Arbeitsspeicher frei. Die Clientanwendung muss den Arbeitsspeicher freigeben, bevor sie beendet wird. Der Serverstub gibt Arbeitsspeicher frei, wenn der Remoteprozeduraufruf zurückgegeben wird (abhängig vom \[ [Attribut allocate](/windows/desktop/Midl/allocate) \] ACF).

 

 