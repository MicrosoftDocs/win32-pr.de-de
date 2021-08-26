---
title: Strategien zur Fehlerbehandlung
description: Strategien zur Fehlerbehandlung
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0527edbb8bab4b4a0b0ca9e0d135bc5cf8c2827497a36fb9cad021680868f764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029970"
---
# <a name="error-handling-strategies"></a>Strategien zur Fehlerbehandlung

Da Schnittstellenmethoden virtuell sind, ist es für einen Aufrufer nicht möglich, den vollständigen Satz von Werten zu kennen, die von einem Aufruf zurückgegeben werden können. Eine Implementierung einer Methode kann fünf Werte zurückgeben. ein anderer kann acht zurückgeben.

In der Dokumentation werden allgemeine Werte aufgeführt, die für jede Methode zurückgegeben werden können. Dies sind die Werte, die Sie im Code überprüfen und verarbeiten müssen, da sie eine besondere Bedeutung haben. Andere Werte werden möglicherweise zurückgegeben, aber da sie nicht aussagekräftig sind, müssen Sie keinen speziellen Code schreiben, um sie zu verarbeiten. Eine einfache Überprüfung auf 0 (null) oder ungleich 0 (null) ist ausreichend.

## <a name="hresult-values"></a>HRESULT-Werte

Der Rückgabewert von COM-Funktionen und -Methoden ist ein **HRESULT.** Die Werte einiger HRESULTs wurden in COM geändert, um alle Duplizierung und Überlappung mit den Systemfehlercodes zu vermeiden. Diejenigen, die Systemfehlercodes duplizieren, wurden in FACILITY WIN32 geändert, und solche, die sich überschneiden, \_ verbleiben in FACILITY \_ NULL. Allgemeine **HRESULT-Werte** und deren Werte sind in der folgenden Tabelle aufgeführt.



| HRESULT                    | Wert                 | BESCHREIBUNG                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ ABORT<br/>        | 0x80004004<br/> | Der Vorgang wurde aufgrund eines nicht angegebenen Fehlers abgebrochen.<br/>                                                                              |
| E \_ ACCESSDENIED<br/> | 0x80070005<br/> | Allgemeiner Fehler "Zugriff verweigert".<br/>                                                                                                          |
| E \_ FAIL<br/>         | 0x80004005<br/> | Es ist ein nicht angegebener Fehler aufgetreten.<br/>                                                                                                    |
| E \_ HANDLE<br/>       | 0x80070006<br/> | Es wurde ein ungültiges Handle verwendet.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Mindestens ein Argument ist ungültig.<br/>                                                                                                      |
| E \_ NOINTERFACE<br/>  | 0x80004002<br/> | Die [**QueryInterface-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) hat die angeforderte Schnittstelle nicht erkannt. Die -Schnittstelle wird nicht unterstützt.<br/> |
| E \_ NOTIMPL<br/>      | 0x80004001<br/> | Die Methode ist nicht implementiert.<br/>                                                                                                          |
| E \_ OUTOFMEMORY<br/>  | 0x8007000E<br/> | Die Methode konnte den erforderlichen Arbeitsspeicher nicht zuordnen.<br/>                                                                                         |
| E \_ AUSSTEHEND<br/>      | 0x8000000A<br/> | Die zum Abschließen des Vorgangs erforderlichen Daten sind noch nicht verfügbar.<br/>                                                                      |
| \_E-ZEIGER<br/>      | 0x80004003<br/> | Ein ungültiger Zeiger wurde verwendet.<br/>                                                                                                            |
| E \_ UNEXPECTED<br/>   | 0x8000FFFF<br/> | Ein schwerwiegender Fehler ist aufgetreten.<br/>                                                                                                    |
| S \_ FALSE<br/>        | 0x00000001<br/> | Die Methode war erfolgreich und hat den booleschen Wert **FALSE zurückgegeben.**<br/>                                                                          |
| S \_ OK<br/>           | 0x00000000<br/> | Die Methode wurde erfolgreich ausgeführt. Wenn ein boolescher Rückgabewert erwartet wird, ist der zurückgegebene Wert **TRUE.**<br/>                                            |



 

## <a name="network-errors"></a>Netzwerkfehler

Wenn die ersten vier Ziffern des Fehlercodes 8007 sind, deutet dies auf einen System- oder Netzwerkfehler hin. Sie können den Befehl **net** verwenden, um diese Arten von Fehlern zu decodieren. Um den Fehler zu decodieren, konvertieren Sie zuerst die letzten vier Ziffern des hexadezimalen Fehlercodes in decimal. Geben Sie dann an der Eingabeaufforderung Folgendes ein, wobei dezimaler Code durch den Rückgabewert ersetzt wird, den Sie decodieren möchten:

**net helpmsg <** _\_ Dezimalcode_*_>_*

Der Befehl net gibt eine Beschreibung des Fehlers zurück. Wenn COM beispielsweise den Fehler 8007054B zurückgibt, konvertieren Sie 054B in decimal (1355). Geben Sie anschließend Folgendes ein:

**net helpmsg 1355**

Der Befehl net gibt die Fehlerbeschreibung zurück: "Die angegebene Domäne war nicht vorhanden".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in COM](error-handling-in-com.md)
</dt> </dl>

 

 





