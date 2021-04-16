---
title: InprocServer32
description: Registriert einen 32-Bit-in-Process-Server und gibt das Threading Modell des Apartment an, in dem der Server ausgeführt werden kann.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515962"
---
# <a name="inprocserver32"></a>InprocServer32

Registriert einen 32-Bit-in-Process-Server und gibt das Threading Modell des Apartment an, in dem der Server ausgeführt werden kann.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Bemerkungen

**ThreadingModel** ist ein **reg \_ SZ** -Wert, der das Threading Modell angibt. Die möglichen Werte sind in der folgenden Tabelle aufgeführt.



| Wert     | BESCHREIBUNG                                |
|-----------|--------------------------------------------|
| Apartment | Single Thread-Apartment                  |
| Both      | Single Thread-oder Multithread-Apartment |
| Kostenlos      | Multithread-Apartment                    |
| Neutral   | Neutrales Apartment                          |



 

Sie müssen für jedes Objekt, das vom Prozess internen Server bereitgestellt wird, denselben Wert verwenden.

Wenn **ThreadingModel** nicht vorhanden oder nicht auf einen Wert festgelegt ist, wird der Server in das erste Apartment geladen, das im Prozess initialisiert wurde. Dieses Apartment wird manchmal als Haupt-Single Thread-Apartment (STA) bezeichnet. Wenn der erste STA in einem Prozess durch com initialisiert wird, anstatt durch einen expliziten Aufruf von [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), wird er als Host STA bezeichnet. Beispielsweise erstellt com einen Host-STA, wenn ein in-Process-Server, der geladen werden soll, einen STA erfordert, aber zurzeit kein STA im Prozess vorhanden ist.

Wenn möglich, wird der Prozess interne Server in dasselbe Apartment geladen wie der Client, der ihn lädt. Wenn das Threading Modell des Client-Apartment nicht mit dem angegebenen Modell kompatibel ist, wird der Server entsprechend der Angabe in der folgenden Tabelle geladen.



| Threading Modell des Servers | Apartment Server wird ausgeführt in |
|---------------------------|----------------------------|
| <not specified>     | Haupt-STA                   |
| Both                      | Dasselbe Apartment wie der Client   |
| Kostenlos                      | Multithread-Apartment    |
| Neutral                   | Neutrales Apartment          |



 

Wenn das Threading Modell des Servers Apartment ist, hängt das Apartment, in das der Server geladen wird, von dem Apartment ab, in dem der Client ausgeführt wird, wie in der folgenden Tabelle aufgeführt.



| Apartment Client wird ausgeführt in | Apartment Server wird ausgeführt in |
|----------------------------|----------------------------|
| Multithread              | Host-STA                   |
| Neutral (auf STA-Thread)    | Dasselbe Apartment wie der Client   |
| Neutral (im MTA-Thread)    | Host-STA                   |



 

COM kann auch einen Host-Multithread-Apartment (MTA) erstellen. Wenn ein Client in einem Single Thread-Apartment einen Prozess internen Server anfordert, dessen Threading Modell frei ist, wenn kein MTA im Prozess vorhanden ist, erstellt com einen Host-MTA und lädt ihn in den Server.

Bei einem in-Process-32-Bit-Server müssen die Schlüssel [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InProcServer32** und [**Insertable**](insertable.md) registriert werden. Der **InprocServer** -Eintrag wird nur aus Gründen der Abwärtskompatibilität benötigt. Wenn Sie fehlt, funktioniert die Klasse weiterhin, aber Sie kann nicht in 16-Bit-Anwendungen geladen werden.

Wenn ein Container die Registrierung nach einem in-Process-Server durchsucht, hat die 16-Bit-Version eine Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat eine Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




