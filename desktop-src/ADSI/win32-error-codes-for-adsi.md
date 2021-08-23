---
title: Win32-Fehlercodes für ADSI
description: Standardmäßige Win32-Fehlercodes werden auch verwendet, um ADSI-Fehlermeldungen zurück zu geben.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Win32-Fehlercodes für ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b18539e93504991f244bbba8b41b13e524ff236918145deda73788169cef368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589740"
---
# <a name="win32-error-codes-for-adsi"></a>Win32-Fehlercodes für ADSI

Standardmäßige Win32-Fehlercodes werden auch verwendet, um ADSI-Fehlermeldungen zurück zu geben. Insbesondere ordnet der ADSI-LDAP-Anbieter alle LDAP-Fehlercodes Win32-Fehlercodes zu. Die **HRESULT-Werte** dieser Fehlercodes haben das Format 0x8007XXXX, wobei die letzten vier Hexadezimalziffern XXXX den **DWORD-Werten** des entsprechenden Win32-Fehlercodes entsprechen. Der ADSI-Fehlerwert 0x80072020 beispielsweise den Win32-Fehlerwert 0x2020 hexadezimal oder 8224 als Dezimalzahl.

Um den **HRESULT-Wert** eines ADSI-Fehlercodes, der von Ihrer Anwendung zurückgegeben wird, in den entsprechenden Win32-Fehler-DWORD-Wert zu konvertieren, wie in den obigen Headerdateien definiert, verwenden Sie das folgende Verfahren. 

Die meisten Win32-Fehlercodes für ADSI sind in Winerror.h oder Lmerr.h definiert. Die Fehlerwerte werden in diesen Dateien als Dezimalwerte aufgeführt.

**So konvertieren Sie den **HRESULT-Wert** eines ADSI-Fehlercodes in den entsprechenden Win32-Fehler-DWORD-Wert**

1.  Konvertieren Sie **den HRESULT-Wert** in eine Hexadezimalzahl, wenn Sie mit einem Dezimalwert beginnen, wie Sie es von einer Visual Basic erhalten.
2.  Wenn Sie den 0x8007, wird der Rest erzeugt.
3.  Konvertiert den Rest in eine Dezimalzahl.
4.  Suchen Sie in Winerror.h nach dem Dezimaltrennzeichen.
5.  Wenn sie in "Winerror.h" nicht gefunden wird, subtrahieren Sie 2100 vom Dezimaltrennzeichen, und suchen Sie das Ergebnis in Lmerr.h.

ADSI 2.0 ordnet die LDAP-Fehlercodes einer Reihe von Win32-Fehlercodes zu, die sich von denen unterscheiden, die in ADSI für Windows 2000 und den DS-Client verwendet werden. Die Unterschiede sind in folgenden Aufgeführt:

-   [Win32-Fehlercodes](win32-error-codes.md)
-   [Win32-Fehlercodes für ADSI 2.0](win32-error-codes-for-adsi-2-0.md)

 

 




