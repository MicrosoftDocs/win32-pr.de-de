---
title: Win32-Fehler Codes für ADSI
description: Standard-Win32-Fehlercodes werden auch zum Zurückgeben von ADSI-Fehlermeldungen verwendet.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Win32-Fehler Codes für ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707349"
---
# <a name="win32-error-codes-for-adsi"></a>Win32-Fehler Codes für ADSI

Standard-Win32-Fehlercodes werden auch zum Zurückgeben von ADSI-Fehlermeldungen verwendet. Insbesondere ordnet der ADSI LDAP-Anbieter alle LDAP-Fehlercodes den Win32-Fehlercodes zu. Die **HRESULT** -Werte dieser Fehlercodes haben das Format 0x8007xxxx, wobei die letzten vier hexadezimalen Ziffern xxxx den **DWORD** -Werten des entsprechenden Win32-Fehlercodes entsprechen. Der ADSI-Fehlerwert 0x80072020 gibt z. b. den Win32-Fehlerwert 0x2020 in Hexadezimal oder 8224 als Dezimalwert an.

Um den **HRESULT** -Wert eines von der Anwendung zurückgegebenen ADSI-Fehlercodes in den entsprechenden Win32- **DWORD** -Wert zu konvertieren, wie in den Header Dateien oben definiert, verwenden Sie das folgende Verfahren.

Die meisten Win32-Fehlercodes für ADSI sind in WinError. h oder lmerr. h definiert. Die Fehler Werte werden in diesen Dateien als Dezimalwerte aufgelistet.

**So konvertieren Sie den **HRESULT** -Wert eines ADSI-Fehlercodes in den entsprechenden Win32-Fehler **DWORD** -Wert**

1.  Konvertieren Sie den **HRESULT** -Wert in eine hexadezimale Zahl, wenn Sie mit einem Dezimalwert beginnen, wie Sie möglicherweise von einer Visual Basic Anwendung erhalten.
2.  Drop The 0x8007 Part erzeugt den Rest.
3.  Konvertiert den Rest in eine Dezimalzahl.
4.  Suchen Sie in WinError. h nach dem Dezimaltrennzeichen.
5.  Wenn Sie in WinError. h nicht gefunden werden, subtrahieren Sie 2100 vom Dezimaltrennzeichen, und suchen Sie das Ergebnis in lmerr. h.

ADSI 2,0 ordnet die LDAP-Fehlercodes einer Reihe von Win32-Fehlercodes zu, die sich von der in ADSI für Windows 2000 und dem DS-Client verwendeten Win32-Fehlercodes unterscheiden. Die Unterschiede sind in aufgeführt:

-   [Win32-Fehler Codes](win32-error-codes.md)
-   [Win32-Fehler Codes für ADSI 2,0](win32-error-codes-for-adsi-2-0.md)

 

 




