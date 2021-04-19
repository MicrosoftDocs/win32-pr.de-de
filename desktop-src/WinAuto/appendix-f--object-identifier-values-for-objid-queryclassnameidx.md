---
title: Anhang F Objekt-ID-Werte für OBJID_QUERYCLASSNAMEIDX
description: Wenn oleacc eine WM- \_ GetObject-Nachricht mit dem lParam-Parameter sendet, die auf objidqueryclassnameidx festgelegt ist, geben viele Standardbenutzer-oder allgemeine Steuerelemente (COMCTL) einen der folgenden Werte zurück.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342364"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Anhang F: objektbezeichnerwerte für objID \_ queryclassnameidx

Wenn oleacc eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht mit dem *LPARAM* -Parameter sendet, die auf objidqueryclassnameidx festgelegt ist, geben viele Standardbenutzer-oder allgemeine Steuerelemente (COMCTL) einen der folgenden Werte zurück.



| Benutzer-oder gängiges Steuerelement | Rückgabewert |
|------------------------|--------------|
| Listenfeld                | 65536 + 0      |
| Schaltfläche                 | 65536 + 2      |
| statischen                 | 65536 + 3      |
| Bearbeiten                   | 65536 + 4      |
| Combobox               | 65536 + 5      |
| Bildlaufleiste              | 65536 + 10     |
| Status                 | 65536 + 11     |
| Symbolleiste                | 65536 + 12     |
| Fortschritt               | 65536 + 13     |
| Belebt                | 65536 + 14     |
| Registerkarte                    | 65536 + 15     |
| Hotkey                 | 65536 + 16     |
| Header                 | 65536 + 17     |
| TrackBar               | 65536 + 18     |
| ListView               | 65536 + 19     |
| UpDown                 | 65536 + 22     |
| Quick Infos               | 65536 + 24     |
| TreeView               | 65536 + 25     |
| RichEdit               | 65536 + 28     |



 

Nur Benutzer und allgemeine Windows-Steuerelemente (COMCTL) geben einen der Werte aus der Tabelle zurück. Wenn ein Fenster als Antwort auf diese Meldung 0 zurückgibt, kann das Fenster eine der folgenden sein:

-   Benutzerdefiniertes Steuerelement
-   Ein anderes Steuerelement als eines der Steuerelemente in der vorherigen Tabelle.
-   Eine alte Version eines System Steuer Elements, das die WM- [**\_ GetObject**](wm-getobject.md) -Nachricht nicht erkennt

Wenn ein Fenster 0 zurückgibt, müssen die Clients möglicherweise " [**realgetwindowclass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) " oder " [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)" verwenden. Sie können diese Funktionen verwenden, um den Typ des Steuer Elements basierend auf dem Klassennamen zu bestimmen.

Im Allgemeinen können Clients die von oleacc bereitgestellten Informationen verwenden.

 

 