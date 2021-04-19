---
title: Sicherheitsüberlegungen Text Services-Framework
description: Sicherheitsüberlegungen Text Services-Framework
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Text Dienst Framework (TSF), Sicherheit
- TSF (Text Dienst Framework), Sicherheit
- Text Dienste, Sicherheit
- TSF-aktivierte Anwendungen, Sicherheit
- Sicherheit für TSF
- Text Dienst Framework (TSF), bewährte Methoden
- TSF (Text Dienst Framework), bewährte Methoden
- TSF-aktivierte Anwendungen, bewährte Methoden
- Text Dienste, bewährte Methoden
- bewährte Methoden für TSF
- Text Services-Framework (TSF), Fehlerüberprüfung
- TSF (Text Dienst Framework), Fehlerüberprüfung
- TSF-aktivierte Anwendungen, Fehlerüberprüfung
- Text Dienste, Fehlerüberprüfung
- Fehlerüberprüfung
- Text Dienst Framework (TSF), digitale Signaturen
- TSF (Text Dienst Framework), digitale Signaturen
- Text Dienste, digitale Signaturen
- TSF-aktivierte Anwendungen, digitale Signaturen
- Digitale Signaturen
- Text Dienst Framework (TSF), LoadLibrary-Aufrufe
- TSF (Text Services Framework), LoadLibrary-Aufrufe
- Text Dienste, LoadLibrary-Aufrufe
- TSF-aktivierte Anwendungen, LoadLibrary-Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342349"
---
# <a name="security-considerations-text-services-framework"></a>Sicherheitsüberlegungen: Text Services-Framework

## <a name="best-practices-for-developing-with-tsf"></a>Bewährte Methoden für die Entwicklung mit TSF

-   **Digitale Signaturen:** Text Dienstanbieter sollten digitale Signaturen mit Ihren binären ausführbaren Dateien bereitstellen. Ein registrierter Text Dienst hat Zugriff auf Systemthreads und kann Informationen verfügbar machen, auf die andernfalls nicht zugegriffen werden kann. Um einen stabilen und sicheren Betrieb sicherzustellen, muss der Benutzer die digitale Signatur eines Text Dienstanbieter überprüfen, bevor der Text Dienst geladen werden darf. Das richtige Verfahren zum Erstellen einer digitalen Signatur finden Sie unter [Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) .
-   **Fehlerüberprüfung:** Jeder Methoden-oder Funktionsaufrufe sollte auf Erfolg geprüft werden. Im Fall eines Fehlers sollten die verbleibenden Methoden-oder Funktionsaufrufe übersprungen werden. Die meisten Codebeispiele in dieser Dokumentation enthalten nur eine begrenzte Fehlerüberprüfung oder gar keine Fehlerüberprüfung, um zu vermeiden, dass der zu Veranschaulichung Punkt verdeckt wird. Sie sollten keine Beispiele aus der Dokumentation direkt in den Produktionscode einfügen. Stattdessen sollten Sie die Beispiele verbessern, indem Sie eine eigene Fehlerüberprüfung hinzufügen.

-   **LoadLibrary-Aufrufe:** Zum Abrufen eines Zeigers auf eine der [TSF-Funktionen](text-services-framework-functions.md)müssen Sie [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)verwenden. Es ist jedoch wichtig, die Prozeduren zum Formatieren des dll-Pfadnamens zu befolgen, wie in der **LoadLibrary** -Dokumentation angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Sicherheitsmethoden](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[TSF-Funktionen](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 