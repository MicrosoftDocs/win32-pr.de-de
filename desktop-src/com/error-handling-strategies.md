---
title: Fehlerbehandlungsstrategien
description: Fehlerbehandlungsstrategien
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c594a8b1e5baf0eab3d928b8f1b861b7f0160d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104472212"
---
# <a name="error-handling-strategies"></a>Fehlerbehandlungsstrategien

Da Schnittstellen Methoden virtuell sind, ist es nicht möglich, dass ein Aufrufer den vollständigen Satz von Werten kennt, die von einem Aufruf zurückgegeben werden können. Eine Implementierung einer Methode kann fünf Werte zurückgeben. eine andere kann acht zurückgeben.

In der Dokumentation werden allgemeine Werte aufgelistet, die für jede Methode zurückgegeben werden können. Dies sind die Werte, die Sie im Code überprüfen und behandeln müssen, da Sie eine besondere Bedeutung haben. Andere Werte können zurückgegeben werden, aber da Sie nicht aussagekräftig sind, müssen Sie keinen speziellen Code schreiben, um Sie zu behandeln. Eine einfache Überprüfung auf NULL oder eine nicht-NULL-Werte ist ausreichend.

## <a name="hresult-values"></a>HRESULT-Werte

Der Rückgabewert von com-Funktionen und-Methoden ist ein **HRESULT**. Die Werte einiger HRESULTs wurden in com geändert, sodass alle Duplizierungen und Überschneidungen mit den Systemfehler Codes vermieden werden. Solche, die doppelte Systemfehler Codes haben, wurden in die \_ Win32-Anlage geändert, und die überlappenden sind in der Anlage \_ NULL. Allgemeine **HRESULT** -Werte und ihre Werte sind in der folgenden Tabelle aufgeführt.



| HRESULT                    | Wert                 | BESCHREIBUNG                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ Abbrechen<br/>        | 0x80004004<br/> | Der Vorgang wurde aufgrund eines nicht angegebenen Fehlers abgebrochen.<br/>                                                                              |
| E \_ AccessDenied<br/> | 0x80070005<br/> | Ein allgemeiner Fehler vom Typ "Zugriff verweigert".<br/>                                                                                                          |
| E \_ fehlschlagen<br/>         | 0x80004005<br/> | Ein nicht angegebener Fehler ist aufgetreten.<br/>                                                                                                    |
| E- \_ handle<br/>       | 0x80070006<br/> | Es wurde ein ungültiges Handle verwendet.<br/>                                                                                                             |
| E \_ invalidArg<br/>   | 0x80070057<br/> | Mindestens ein Argument ist ungültig.<br/>                                                                                                      |
| E \_ nointerface<br/>  | 0x80004002<br/> | Die [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode hat die angeforderte Schnittstelle nicht erkannt. Die-Schnittstelle wird nicht unterstützt.<br/> |
| E \_ notimpl<br/>      | 0x80004001<br/> | Die Methode ist nicht implementiert.<br/>                                                                                                          |
| E \_ outo-Memory<br/>  | 0x8007000E<br/> | Die Methode konnte den erforderlichen Arbeitsspeicher nicht zuordnen.<br/>                                                                                         |
| E \_ Ausstehend<br/>      | 0x8000000A<br/> | Die für den Vorgang erforderlichen Daten sind noch nicht verfügbar.<br/>                                                                      |
| E- \_ Zeiger<br/>      | 0x80004003<br/> | Ein ungültiger Zeiger wurde verwendet.<br/>                                                                                                            |
| E \_ unerwartet<br/>   | 0x8000FFFF<br/> | Ein schwerwiegender Fehler ist aufgetreten.<br/>                                                                                                    |
| S \_ false<br/>        | 0x00000001<br/> | Die Methode war erfolgreich und hat den booleschen Wert " **false**" zurückgegeben.<br/>                                                                          |
| S \_ OK<br/>           | 0x00000000<br/> | Die Methode wurde erfolgreich ausgeführt. Wenn ein boolescher Rückgabewert erwartet wird, ist der zurückgegebene Wert **true**.<br/>                                            |



 

## <a name="network-errors"></a>Netzwerkfehler

Wenn die ersten vier Ziffern des Fehlercodes 8007 lauten, weist dies auf einen System-oder Netzwerkfehler hin. Sie können den **net** -Befehl verwenden, um diese Arten von Fehlern zu decodieren. Um den Fehler zu decodieren, konvertieren Sie zuerst die letzten vier Ziffern des hexadezimalen Fehlercodes in Decimal. Geben Sie dann an der Eingabeaufforderung Folgendes ein, wobei der Dezimal Code durch den Rückgabewert ersetzt wird, den Sie decodieren möchten:

**net helpmsg <***Decimal- \_ Code***>**

Der NET-Befehl gibt eine Beschreibung des Fehlers zurück. Wenn com z. b. den Fehler 8007054b zurückgibt, konvertieren Sie 054b in Decimal (1355). Geben Sie anschließend Folgendes ein:

**net helpmsg 1355**

Der NET-Befehl gibt die Fehlerbeschreibung zurück: "die angegebene Domäne ist nicht vorhanden".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](error-handling-in-com.md)
</dt> </dl>

 

 





