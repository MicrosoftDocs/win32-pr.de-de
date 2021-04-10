---
title: Grundlagen der strukturierten Speicherung
description: Der strukturierte Speicher bietet das Äquivalent zu einem kompletten Dateisystem zum Speichern von Objekten.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Strukturierter Speicherplatz Halter, Grundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858316"
---
# <a name="structured-storage-fundamentals"></a>Grundlagen der strukturierten Speicherung

Der strukturierte Speicher stellt die Entsprechung eines kompletten Dateisystems zum Speichern von Objekten mithilfe der in der folgenden Tabelle aufgeführten Elemente dar.



| Element                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strukturierte Speicher Schnittstellen](structured-storage-interfaces.md)       | Die Schnittstellen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)und [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) sowie eine Reihe verwandter Schnittstellen –[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)und [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). |
| [Strukturierte Speicher-API-Funktionen](structured-storage-api-functions.md) | Hilfsobjekte, die eine Implementierung von strukturiertem Speicher und einen zweiten Satz von APIs für Verbund Dateien vereinfachen. Dies ist die com-Implementierung der strukturierten Speicher Schnittstellen. COM bietet auch eine Reihe unterstützter Strukturen und Enumerationswerte, die zum Organisieren von Parametern für Schnittstellen Methoden und APIs verwendet werden.                              |
| [Strukturierte Speicherzugriffs Modi](structured-storage-access-modes.md)   | Ein Satz von Zugriffs Modi zum Steuern des Zugriffs auf Verbund Dateien.                                                                                                                                                                                                                                                                                                 |



 

 

 