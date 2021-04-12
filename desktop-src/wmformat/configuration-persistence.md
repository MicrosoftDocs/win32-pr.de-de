---
title: Konfigurations Persistenz
description: Konfigurations Persistenz
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media-Format-SDK, Persistenz
- Windows Media-Format-SDK, Konfigurations Persistenz
- Advanced Systems Format (ASF), Persistenz
- ASF (Advanced Systems Format), Persistenz
- Advanced Systems Format (ASF), Konfigurations Persistenz
- ASF (Advanced Systems Format), Konfigurations Persistenz
- Konfigurations Persistenz
- Dauerhaftigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389926"
---
# <a name="configuration-persistence"></a>Konfigurations Persistenz

Keine der in dieser Dokumentation beschriebenen Schreib aktivierten Eigenschaften wird vom Windows Media SDK gespeichert. Jede Anwendung, die das SDK verwendet, muss bei Bedarf eigene persistenzprozeduren bereitstellen und die entsprechende Set-Methode für jede Instanz des SDK aufrufen. Auf diese Weise wirken sich Konfigurationsänderungen, die von einer Anwendung vorgenommen werden, nicht auf eine andere Anwendung aus. Beispielsweise wirkt sich das Ändern der Pufferzeit in einem Player nicht auf einen anderen Player aus.

Die einzige Ausnahme von dieser Regel sind die Informationen zu den Anmelde Informationen. Wenn die Anwendung anzeigt, dass die Benutzer-ID und die Kenn Wort Informationen in der Rückgabe vom **acquirecredensted** -Befehl beibehalten werden müssen, speichert das SDK diese Informationen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> <dt>

[**Iwmkredentialcallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




