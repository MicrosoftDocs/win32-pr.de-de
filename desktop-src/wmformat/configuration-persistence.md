---
title: Konfigurationspersistenz
description: Konfigurationspersistenz
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Medienformat-SDK, Persistenz
- Windows Medienformat-SDK, Konfigurationspersistenz
- Advanced Systems Format (ASF), Persistenz
- ASF (Advanced Systems Format), Persistenz
- Advanced Systems Format (ASF), Konfigurationspersistenz
- ASF (Advanced Systems Format), Konfigurationspersistenz
- Konfigurationspersistenz
- Dauerhaftigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b5b2442779fb709299f42e0194317aadaf54a51cd4946e61adf7a90a50957d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434357"
---
# <a name="configuration-persistence"></a>Konfigurationspersistenz

Keine der in dieser Dokumentation beschriebenen Eigenschaften mit aktivierten Schreibzugriffen wird vom Windows Media SDK gespeichert. Jede Anwendung, die das SDK verwendet, muss bei Bedarf eigene Persistenzverfahren bereitstellen und die entsprechende set-Methode für jede Instanz des SDK aufrufen. Auf diese Weise wirken sich Konfigurationsänderungen, die von einer Anwendung vorgenommen werden, nicht auf eine andere Anwendung aus. Das Ändern der Pufferzeit in einem Player wirkt sich beispielsweise nicht auf einen anderen Player aus.

Die einzige Ausnahme von dieser Regel sind die Anmeldeinformationen. Wenn die Anwendung in der Rückgabe des **AcquireCredentials-Aufrufs** angibt, dass die Benutzer-ID und das Kennwort beibehalten werden müssen, speichert das SDK diese Informationen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> <dt>

[**IWMCredentialCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




