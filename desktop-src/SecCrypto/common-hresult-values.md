---
description: Die folgenden HRESULT-Werte werden am häufigsten verwendet. Weitere Werte sind in der Headerdatei Winerror.h enthalten.
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: Allgemeine HRESULT-Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b23b43a23629fdd74770a3269c40dba6746b549bd9300c271c8ee5406ed9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769429"
---
# <a name="common-hresult-values"></a>Allgemeine HRESULT-Werte

Die folgenden HRESULT-Werte werden am häufigsten verwendet. Weitere Werte sind in der Headerdatei Winerror.h enthalten.

Hier sind die Werte alphabetisch nach Namen aufgeführt.



| Name            | Beschreibung                         | Wert      |
|-----------------|-------------------------------------|------------|
| S \_ OK           | Vorgang erfolgreich                | 0x00000000 |
| E \_ ABORT        | Vorgang abgebrochen                   | 0x80004004 |
| E \_ ACCESSDENIED | Fehler "Allgemeiner Zugriff verweigert"         | 0x80070005 |
| E \_ FAIL         | Nicht angegebener Fehler                 | 0x80004005 |
| E \_ HANDLE       | Ungültiges Handle            | 0x80070006 |
| E \_ INVALIDARG   | Mindestens ein Argument ist ungültig. | 0x80070057 |
| E \_ NOINTERFACE  | Schnittstelle nicht unterstützt.         | 0x80004002 |
| E \_ NOTIMPL      | Nicht implementiert                     | 0x80004001 |
| E \_ OUTOFMEMORY  | Fehler beim Zuordnen des erforderlichen Arbeitsspeichers | 0x8007000E |
| \_E-ZEIGER      | Ungültiger Zeiger           | 0x80004003 |
| E \_ UNEXPECTED   | Unerwarteter Fehler                  | 0x8000FFFF |



 

Hier sind die Werte in numerischer Reihenfolge nach Wert aufgeführt.



| Wert      | Name            | Beschreibung                         |
|------------|-----------------|-------------------------------------|
| 0x00000000 | S \_ OK           | Vorgang erfolgreich                |
| 0x80004001 | E \_ NOTIMPL      | Nicht implementiert                     |
| 0x80004002 | E \_ NOINTERFACE  | Schnittstelle nicht unterstützt.         |
| 0x80004003 | \_E-ZEIGER      | Ungültiger Zeiger           |
| 0x80004004 | E \_ ABORT        | Vorgang abgebrochen                   |
| 0x80004005 | E \_ FAIL         | Nicht angegebener Fehler                 |
| 0x8000FFFF | E \_ UNEXPECTED   | Unerwarteter Fehler                  |
| 0x80070005 | E \_ ACCESSDENIED | Fehler "Allgemeiner Zugriff verweigert"         |
| 0x80070006 | E \_ HANDLE       | Ungültiges Handle            |
| 0x8007000E | E \_ OUTOFMEMORY  | Fehler beim Zuordnen des erforderlichen Arbeitsspeichers |
| 0x80070057 | E \_ INVALIDARG   | Mindestens ein Argument ist ungültig. |



 

 

 



