---
title: Die neuen Datentypen
description: Es wurden drei Klassen von Datentypen für 64-Bit-Windows-Datentypen mit fester Genauigkeit, Zeiger Genauigkeit und spezifische Zeiger Genauigkeit eingeführt.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Datentypen
- Datentypen 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cf5960b5344da1d459d12dee96a2f67f2cfbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316215"
---
# <a name="the-new-data-types"></a>Die neuen Datentypen

Es wurden drei Klassen von Datentypen für 64-Bit-Windows eingeführt: Datentypen mit fester Genauigkeit, Typen von Zeiger Genauigkeit und Typen spezifischer Zeiger Genauigkeit. Diese Typen wurden der Entwicklungsumgebung hinzugefügt, damit Entwickler sich für 64-Bit-Windows vorbereiten können. Diese Typen werden von der grundlegenden C-Sprache Integer und Long-Typen abgeleitet. Daher können Sie diese Datentypen in Code verwenden, den Sie auf 32-Bit-Fenstern kompilieren und testen, und dann mit dem 64-Bit-Compiler neu kompilieren, wenn Sie auf 64-Bit-Windows abzielen.

Auch bei Anwendungen, die nur 32-Bit-Windows als Ziel haben, wird der Code durch die Einführung dieser neuen Datentypen robuster. Um diese Datentypen verwenden zu können, müssen Sie Ihren Code auf potenziell unsichere Zeiger Verwendung, Polymorphie und Daten Definitionen überprüfen. Wenn eine Variable z. b. den Typ **ulong \_ ptr** hat, ist klar, dass Sie für das Umwandeln von Zeigern für arithmetische Operationen oder Polymorphie verwendet wird. Es ist nicht möglich, eine solche Verwendung direkt mithilfe der älteren Datentypen anzugeben. (Sie können dies indirekt mit abgeleiteter Typbenennung oder ungarischer Notation tun, beide Verfahren sind jedoch fehleranfällig.)

Alle diese Datentypen sind in basetsd. h deklariert. Weitere Informationen, einschließlich Definitionen dieser Datentypen, finden Sie unter [Windows-Datentypen](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Feste Genauigkeit

Datentypen mit fester Genauigkeit haben dieselbe Länge in 32-und 64-Bit-Fenstern. Um Sie dabei zu unterstützen, ist Ihre Genauigkeit Teil des Namens des Datentyps. Im folgenden finden Sie die Datentypen mit fester Genauigkeit.



| Begriff                                                                       | BESCHREIBUNG                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | 32-Bit-Ganzzahl ohne Vorzeichen<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | 64-Bit-Ganzzahl ohne Vorzeichen<br/> |
| <span id="INT32"></span><span id="int32"></span>**Int32**<br/>       | 32-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="INT64"></span><span id="int64"></span>**Int64**<br/>       | 64-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | 32-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | 64-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UInt32**<br/>    | Nicht signiertes **Int32**<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | Nicht signiertes **Int64**<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | Nicht signiertes **LONG32**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | Nicht signiertes **LONG64**<br/>     |



 

## <a name="pointer-precision"></a>Zeiger Genauigkeit

Wenn die Zeiger Genauigkeit geändert wird (d. h., da Sie 32 Bits auf 32-Bit-Fenstern und 64 Bits mit 64-Bit-Fenstern ist), spiegeln die Datentypen der Zeiger Genauigkeit die Genauigkeit entsprechend wider. Daher ist es sicher, bei der Ausführung von Zeigerarithmetik einen Zeiger auf einen dieser Typen umzuwandeln. Wenn die Zeiger Genauigkeit 64 Bits beträgt, ist der Typ 64 Bits. Die Anzahl Typen geben außerdem die maximale Größe an, auf die ein Zeiger verweisen kann. Im folgenden finden Sie die Typen "Zeiger Genauigkeit" und "Anzahl".



| Begriff                                                                              | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**DWORD \_ ptr**<br/> | Long-Typ ohne Vorzeichen für Zeiger Genauigkeit.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**halbe \_ ptr**<br/>    | Die Hälfte der Größe eines Zeigers. Verwenden Sie innerhalb einer-Struktur, die einen Zeiger und zwei kleine Felder enthält.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ ptr**<br/>       | Ganzzahliger Typ mit Vorzeichen für Zeiger Genauigkeit.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**Long- \_ ptr**<br/>    | Long-Typ mit Vorzeichen für Zeiger Genauigkeit.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**Größe \_ T**<br/>          | Die maximale Anzahl von Bytes, auf die ein Zeiger verweisen kann. Verwenden Sie für einen Zähler, der den vollständigen Bereich eines Zeigers umfassen muss.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**ssize \_ T**<br/>       | Signierte **Größe \_ T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**\_uhalbptr**<br/> | Nicht signierte **halbe \_ ptr**.<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**uint \_ ptr**<br/>    | Unsigned **int \_ ptr**.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG \_ ptr**<br/> | Unsigned **Long- \_ ptr**.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Bestimmte Pointer-Precision Typen

Die folgenden neuen Zeiger Typen verfügen explizit über die Größe des Zeigers. Seien Sie vorsichtig, wenn Sie Zeiger im 64-Bit-Code verwenden: Wenn Sie den Zeiger mit einem 32-Bit-Typ deklarieren, erstellt das Betriebssystem den Zeiger durch Abschneiden eines 64-Bit-Zeigers. (Alle Zeiger sind 64 Bits auf 64-Bit-Fenstern.)



| Begriff                                                                                 | BESCHREIBUNG                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**Zeiger \_ 32**<br/> | Ein 32-Bit-Zeiger. Bei 32-Bit-Fenstern handelt es sich hierbei um einen nativen Zeiger. Bei 64-Bit-Fenstern handelt es sich hierbei um einen abgeschnittene 64-Bit-Zeiger.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**Zeiger \_ 64**<br/> | Ein 64-Bit-Zeiger. Bei 64-Bit-Fenstern handelt es sich hierbei um einen nativen Zeiger. Bei 32-Bit-Fenstern ist dies ein mit Vorzeichen erweiterter 32-Bit-Zeiger. <br/> Beachten Sie, dass es nicht sicher ist, dass der Status des hohen Zeiger Bits angenommen wird.<br/> |



 

 

