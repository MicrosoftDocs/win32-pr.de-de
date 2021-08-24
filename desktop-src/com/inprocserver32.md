---
title: Inprocserver32
description: Registriert einen 32-Bit-In-Process-Server und gibt das Threadingmodell des Apartments an, in dem der Server ausgeführt werden kann.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9904aa636bbfb8dc0bc01cac85e041aedfcd34364bd62ac7b0e4e5a9f904750f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567820"
---
# <a name="inprocserver32"></a>Inprocserver32

Registriert einen 32-Bit-In-Process-Server und gibt das Threadingmodell des Apartments an, in dem der Server ausgeführt werden kann.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Hinweise

**ThreadingModel ist** ein **REG \_ SZ-Wert,** der das Threadingmodell angibt. Die möglichen Werte sind in der folgenden Tabelle aufgeführt.



| Wert     | Beschreibung                                |
|-----------|--------------------------------------------|
| Wohnung | Singlethread-Apartment                  |
| Beide      | Singlethread- oder Multithread-Apartment |
| Free      | Multithread-Apartment                    |
| Neutral   | Neutrales Apartment                          |



 

Sie müssen den gleichen Wert für jedes Objekt verwenden, das vom Prozessserver bereitgestellt wird.

Wenn **ThreadingModel** nicht vorhanden oder nicht auf einen Wert festgelegt ist, wird der Server in das erste Apartment geladen, das im Prozess initialisiert wurde. Dieses Apartment wird manchmal als Haupt-Singlethread-Apartment (STA) bezeichnet. Wenn das erste STA in einem Prozess nicht durch einen expliziten Aufruf von [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)sondern durch COM initialisiert wird, wird es als Host-STA bezeichnet. COM erstellt z. B. ein Host-STA, wenn ein zu ladenden Prozessserver ein STA erfordert, aber derzeit kein STA im Prozess ist.

Wenn möglich, wird der Prozessserver im selben Apartment wie der Client geladen, der ihn lädt. Wenn das Threadingmodell des Clienta apartment nicht mit dem angegebenen Modell kompatibel ist, wird der Server geladen, wie in der folgenden Tabelle angegeben.



| Threadingmodell des Servers | Apartmentserver wird in ausgeführt |
|---------------------------|----------------------------|
| <not specified>     | Haupt-STA                   |
| Beide                      | Das gleiche Apartment wie der Client   |
| Free                      | Multithread-Apartment    |
| Neutral                   | Neutrales Apartment          |



 

Wenn das Threadingmodell des Servers Apartment ist, hängt das Apartment, in dem der Server geladen wird, von dem Apartment ab, in dem der Client ausgeführt wird, wie in der folgenden Tabelle angegeben.



| Der Apartmentclient wird in ausgeführt. | Apartmentserver wird in ausgeführt |
|----------------------------|----------------------------|
| Multithreaded              | Host-STA                   |
| Neutral (im STA-Thread)    | Das gleiche Apartment wie der Client   |
| Neutral (im MTA-Thread)    | Host-STA                   |



 

COM kann auch ein Host-Multithread-Apartment (MTA) erstellen. Wenn ein Client in einem Singlethread-Apartment einen Prozessserver an fordert, dessen Threadingmodell Free ist, wenn kein MTA im Prozess ist, erstellt COM einen Host-MTA und lädt den Server in diesen.

Für einen 32-Bit-In-Process-Server müssen die Schlüssel [**InprocHandler32,**](inprochandler32.md) [**InprocServer,**](inprocserver.md) **InprocServer32** und [**Insertable**](insertable.md) registriert werden. Der **Eintrag InprocServer** wird nur aus Gründen der Abwärtskompatibilität benötigt. Wenn sie fehlt, funktioniert die -Klasse weiterhin, kann aber nicht in 16-Bit-Anwendungen geladen werden.

Wenn ein Container die Registrierung nach einem Prozessserver durch sucht, hat die 16-Bit-Version Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




