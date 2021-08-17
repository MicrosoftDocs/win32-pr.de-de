---
title: Sicherheitsüberlegungen Textdienstframework
description: Sicherheitsüberlegungen Textdienstframework
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Textdienstframework (TSF),Sicherheit
- TSF (Textdienstframework),Sicherheit
- Textdienste,Sicherheit
- TSF-fähige Anwendungen, Sicherheit
- Sicherheit für TSF
- Textdienstframework (TSF), bewährte Methoden
- TSF (Textdienstframework), bewährte Methoden
- TSF-fähige Anwendungen, bewährte Methoden
- Textdienste, bewährte Methoden
- Bewährte Methoden für TSF
- Textdienstframework (TSF), Fehlerüberprüfung
- TSF (Textdienstframework),Fehlerüberprüfung
- TSF-fähige Anwendungen, Fehlerüberprüfung
- Textdienste, Fehlerüberprüfung
- Fehlerüberprüfung
- Textdienstframework (TSF), digitale Signaturen
- TSF (Textdienstframework),digitale Signaturen
- Textdienste, digitale Signaturen
- TSF-fähige Anwendungen, digitale Signaturen
- Digitale Signaturen
- Textdienstframework (TSF),LoadLibrary-Aufrufe
- TSF (Textdienstframework),LoadLibrary-Aufrufe
- Textdienste, LoadLibrary-Aufrufe
- TSF-fähige Anwendungen, LoadLibrary-Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432418fbcb6221082083d6595aa374939bc2f4d5cf5aad145cac87444e75bdc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873575"
---
# <a name="security-considerations-text-services-framework"></a>Sicherheitsüberlegungen: Textdienstframework

## <a name="best-practices-for-developing-with-tsf"></a>Bewährte Methoden für die Entwicklung mit TSF

-   **Digitale Signaturen:** Textdienstanbieter sollten digitale Signaturen mit ihren binären ausführbaren Dateien bereitstellen. Ein registrierter Textdienst hat Zugriff auf Systemthreads und kann Informationen verfügbar machen, auf die andernfalls nicht zugegriffen werden kann. Um einen stabilen und sicheren Betrieb sicherzustellen, sollte der Benutzer die digitale Signatur eines Textdiensts überprüfen, bevor der Textdienst geladen werden kann. Informationen zum richtigen Verfahren zum Erstellen einer digitalen Signatur finden Sie unter Einführung in die [Codesignierung.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   **Fehlerüberprüfung:** Jeder Methoden- oder Funktionsaufruf sollte auf Erfolg überprüft werden. Bei einem Fehler sollten die verbleibenden Methoden- oder Funktionsaufrufe übersprungen werden. Die meisten Codebeispiele in dieser Dokumentation haben eine eingeschränkte Fehlerüberprüfung oder gar keine, um zu vermeiden, dass der zu veranschaulichende Punkt verdeckt wird. Sie sollten Beispiele aus der Dokumentation nicht direkt in Produktionscode einfügen. Stattdessen sollten Sie die Beispiele verbessern, indem Sie Eine eigene Fehlerüberprüfung hinzufügen.

-   **LoadLibrary-Aufrufe:** Um einen Zeiger auf eine der [TSF-Funktionen](text-services-framework-functions.md)abzurufen, müssen Sie [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)verwenden. Es ist jedoch wichtig, die Verfahren zum Formatieren des DLL-Pfadnamens zu befolgen, wie in der **LoadLibrary-Dokumentation** angegeben.

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

 

 