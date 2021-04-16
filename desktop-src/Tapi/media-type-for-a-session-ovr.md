---
description: Der Medientyp (oder-Modus) beschreibt den Typ der auszutauschenden Informationen, z. b. interaktive Stimme. Eine bestimmte Kommunikationssitzung kann mehrere Medientypen umfassen.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Medientyp für eine Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530512"
---
# <a name="media-type-for-a-session"></a>Medientyp für eine Sitzung

Der Medientyp (oder-Modus) beschreibt den Typ der auszutauschenden Informationen, z. b. interaktive Stimme. Eine bestimmte Kommunikationssitzung kann mehrere Medientypen umfassen.

Dienstanbieter machen für TAPI und Anwendungen den Medientyp verfügbar, den Sie unterstützen. Informationen zum Erwerb dieser Daten finden Sie in der Übersicht über den Geräte [Medientyp](media-type-ovr.md) .

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**linesetmediamode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**linemonitormedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**line \_ monitormedia**](./line-monitormedia.md) Message, [linemediamode \_ Konstanten](./linemediamode--constants.md).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **cil \_ mediatypesavailable**, [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **cil \_ mediatypesavailable**, [**itcallinfochangeevent:: get \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (gibt die [**callinfochange- \_ Ursache**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) von **CIC \_ mediaType** zurück), [tapimediatype \_ Konstanten](tapimediatype--constants.md).

 

 
