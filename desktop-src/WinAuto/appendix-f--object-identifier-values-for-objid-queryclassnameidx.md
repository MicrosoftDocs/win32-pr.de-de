---
title: Anhang F – Objektbezeichnerwerte für OBJID_QUERYCLASSNAMEIDX
description: Wenn OLEACC eine WM \_ GETOBJECT-Nachricht sendet, bei der der lParam-Parameter auf OBJIDQUERYCLASSNAMEIDX festgelegt ist, geben viele STANDARD-USER- oder COMMON-Steuerelemente (COMCTL) einen der folgenden Werte zurück.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22368f15fa40e30f909f9ad838cb478ed1e9a9c9ff25929f63bb91ec99e99b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134033"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Anhang F: Objektbezeichnerwerte für OBJID \_ QUERYCLASSNAMEIDX

Wenn OLEACC eine [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) sendet, bei der der *lParam-Parameter* auf OBJIDQUERYCLASSNAMEIDX festgelegt ist, geben viele STANDARD-USER- oder COMMON-Steuerelemente (COMCTL) einen der folgenden Werte zurück.



| USER oder allgemeines Steuerelement | Rückgabewert |
|------------------------|--------------|
| Listenfeld                | 65536+0      |
| Schaltfläche                 | 65536+2      |
| statischen                 | 65536+3      |
| Bearbeiten                   | 65536+4      |
| Combobox               | 65536+5      |
| Bildlaufleiste              | 65536+10     |
| Status                 | 65536+11     |
| Symbolleiste                | 65536+12     |
| Fortschritt               | 65536+13     |
| Animieren                | 65536+14     |
| Registerkarte                    | 65536+15     |
| Hotkey                 | 65536+16     |
| Header                 | 65536+17     |
| Trackbar               | 65536+18     |
| Listview               | 65536+19     |
| Updown                 | 65536+22     |
| Quickinfos               | 65536+24     |
| Treeview               | 65536+25     |
| RichEdit               | 65536+28     |



 

Nur USER und Windows common controls (COMCTL) geben einen der Werte aus der Tabelle zurück. Wenn ein Fenster als Antwort auf diese Meldung 0 zurückgibt, kann es sich um eines der folgenden Fenster handelt:

-   Ein benutzerdefiniertes Steuerelement
-   Ein anderes Steuerelement als eines der Steuerelemente in der vorherigen Tabelle
-   Eine alte Version eines Systemsteuerelements, das die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) nicht erkennt

Wenn ein Fenster 0 zurückgibt, müssen Clients möglicherweise [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) oder [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)verwenden. Sie können diese Funktionen verwenden, um den Typ des Steuerelements basierend auf dem Klassennamen zu bestimmen.

Im Allgemeinen können Clients die von OLEACC bereitgestellten Informationen verwenden.

 

 