---
description: Die IME-Fensterklasse ist eine vordefinierte globale Systemklasse, die die Darstellung und das Verhalten der STANDARD-IME-Fenster definiert.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: IME-Fensterklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56449534467a2b01ce8e59991bfc1c5f5ad4e1a9156f86cee5e154a8b8eb1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107190"
---
# <a name="ime-window-class"></a>IME-Fensterklasse

Die IME-Fensterklasse ist eine vordefinierte globale Systemklasse, die die Darstellung und das Verhalten der STANDARD-IME-Fenster definiert. Die -Klasse ähnelt allgemeinen Steuerelementklassen, da die Anwendung mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ein Fenster dieser Klasse erstellt. Wie statische Steuerelemente reagiert ein IME-Fenster nicht selbst auf Benutzereingaben. Stattdessen benachrichtigt er den IME über Benutzereingabeaktionen und verarbeitet Steuerungsmeldungen, die vom IME oder von Anwendungen an ihn gesendet werden, um eine Antwort auf die Benutzeraktion durchzuführen.

IME-orientierte Anwendungen erstellen manchmal benutzerdefinierte IME-Fenster mithilfe der IME-Fensterklasse. Die Verwendung der Fensteranpassung ermöglicht es der Anwendung, die Standardverarbeitung des IME-Fensters zu nutzen und gleichzeitig die Fensterpositionierung zu steuern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Eingabemethode-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
