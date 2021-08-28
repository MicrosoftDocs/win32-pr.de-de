---
title: Die neuen Datentypen
description: Drei Klassen von Datentypen wurden für 64-Bit-Windows-Datentypen mit fester Genauigkeit, Zeigergenauigkeitstypen und typen mit bestimmter Zeigergenauigkeit eingeführt.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows Programmierung , Datentypen
- Datentypen 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc3cc6615de7c93c805eac868536b53084a694fb79d4e63d908716eb026eb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504840"
---
# <a name="the-new-data-types"></a>Die neuen Datentypen

Für 64-Bit-Datentypen wurden drei Klassen Windows eingeführt: Datentypen mit fester Genauigkeit, Zeigergenauigkeitstypen und Typen mit bestimmter Zeigergenauigkeit. Diese Typen wurden der Entwicklungsumgebung hinzugefügt, um Entwicklern die Vorbereitung auf 64-Bit-Windows. Diese Typen werden von den grundlegenden Ganzzahl- und Long-Typen der C-Sprache abgeleitet. Daher können Sie diese Datentypen in Code verwenden, den Sie kompilieren und auf 32-Bit-Windows testen und dann mit dem 64-Bit-Compiler neu kompilieren, wenn Sie 64-Bit-Windows.

Selbst für Anwendungen, die nur 32-Bit-Windows, wird Ihr Code durch die Einführung dieser neuen Datentypen stabiler. Um diese Datentypen zu verwenden, müssen Sie den Code auf potenziell unsichere Zeigerverwendung, Polymorphie und Datendefinitionen überprüfen. Wenn beispielsweise eine Variable vom Typ **ULONG \_ PTR** ist, ist klar, dass sie zum Umwandlungszeigen von Zeigern für arithmetische Operationen oder Polymorphie verwendet wird. Es ist nicht möglich, eine solche Verwendung direkt mithilfe der älteren Datentypen anzugeben. (Sie können dies indirekt tun, indem Sie die Abgeleitete Typbenennung oder die notation -Klasse verwenden, aber beide Techniken sind fehleranfällig.)

Alle diese Datentypen werden in BaseTsd.h deklariert. Weitere Informationen, einschließlich Definitionen dieser Datentypen, finden Sie unter [Windows Datentypen](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Feste Genauigkeit

Datentypen mit fester Genauigkeit haben in 32- und 64-Bit-Windows. Damit Sie sich dies merken können, ist ihre Genauigkeit Teil des Namens des Datentyps. Im Folgenden finden Sie die Datentypen mit fester Genauigkeit.



| Begriff                                                                       | BESCHREIBUNG                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | 32-Bit-Ganzzahl ohne Vorzeichen<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | 64-Bit-Ganzzahl ohne Vorzeichen<br/> |
| <span id="INT32"></span><span id="int32"></span>**INT32**<br/>       | 32-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | 64-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | 32-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | 64-Bit-Ganzzahl mit Vorzeichen<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | Unsigned **INT32**<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | Nicht signiertes **INT64**<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**Ulong32**<br/> | Unsigned **LONG32**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | Unsigned **LONG64**<br/>     |



 

## <a name="pointer-precision"></a>Zeigergenauigkeit

Wenn sich die Zeigergenauigkeit ändert (d. h. 32 Bits auf 32-Bit-Windows und 64 Bit mit 64-Bit-Windows), spiegeln die Zeigergenauigkeitsdatentypen die Genauigkeit entsprechend wider. Daher ist es sicher, einen Zeiger auf einen dieser Typen zu casten, wenn Zeigerarithmetik durchgeführt wird. Wenn die Zeigergenauigkeit 64 Bits beträgt, beträgt der Typ 64 Bits. Die Anzahltypen spiegeln auch die maximale Größe wider, auf die ein Zeiger verweisen kann. Im Folgenden finden Sie die Zeigergenauigkeits- und Anzahltypen.



| Begriff                                                                              | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**DWORD \_ PTR**<br/> | Long-Typ ohne Vorzeichen für Zeigergenauigkeit.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**HALF \_ PTR**<br/>    | Die Hälfte der Größe eines Zeigers. Verwenden Sie in einer -Struktur, die einen Zeiger und zwei kleine Felder enthält.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ PTR**<br/>       | Ganzzahliger Typ mit Vorzeichen für Zeigergenauigkeit.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**LONG \_ PTR**<br/>    | Long-Typ mit Vor signed für Zeigergenauigkeit.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**GRÖßE \_ T**<br/>          | Die maximale Anzahl von Bytes, auf die ein Zeiger verweisen kann. Verwenden Sie für eine Anzahl, die den gesamten Bereich eines Zeigers umfassen muss.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | Signierte **GRÖßE \_ T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ PTR**<br/> | Unsigned **HALF \_ PTR**.<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**UINT \_ PTR**<br/>    | Unsigned **INT \_ PTR**.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG \_ PTR**<br/> | Unsigned **LONG \_ PTR**.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Spezifische Pointer-Precision Typen

Die folgenden neuen Zeigertypen verwenden die explizite Größe des Zeigers. Seien Sie vorsichtig, wenn Sie Zeiger in 64-Bit-Code verwenden: Wenn Sie den Zeiger mit einem 32-Bit-Typ deklarieren, erstellt das Betriebssystem den Zeiger, indem ein 64-Bit-Zeiger abgeschnitten wird. (Alle Zeiger sind 64 Bit auf 64-Bit-Windows.)



| Begriff                                                                                 | BESCHREIBUNG                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**ZEIGER \_ 32**<br/> | Ein 32-Bit-Zeiger. Auf 32-Bit-Windows ist dies ein nativer Zeiger. Auf 64-Bit-Windows ist dies ein abgeschnittener 64-Bit-Zeiger.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**ZEIGER \_ 64**<br/> | Ein 64-Bit-Zeiger. Auf 64-Bit-Windows ist dies ein nativer Zeiger. Auf 32-Bit-Windows ist dies ein erweiterter 32-Bit-Zeiger mit Vorzeichen. <br/> Beachten Sie, dass es nicht sicher ist, den Zustand des Hochzeigerbits anzunehmen.<br/> |



 

 

