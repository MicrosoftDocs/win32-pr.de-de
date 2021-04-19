---
description: Die Konfiguration von IPSec-Richtlinien und Sicherheits Zuordnungen für IPv6 erfolgt mit Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346940"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

Die Konfiguration von IPSec-Richtlinien und Sicherheits Zuordnungen für IPv6 erfolgt mit Ipsec6.exe. Im folgenden finden Sie Ipsec6.exe Unterbefehle:

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**dem ipsec6 SP \[** _Schnittstelle_*_\]_*
</dt> <dd>

Zeigt aktive Sicherheitsrichtlinien an. Zeigt alternativ aktive Sicherheitsrichtlinien für eine bestimmte Schnittstelle an.

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**dem ipsec6 SA**
</dt> <dd>

Zeigt aktive Sicherheits Zuordnungen an.

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**dem ipsec6 c \[** _Dateiname (ohne Erweiterung)_*_\]_*
</dt> <dd>

Erstellt Dateien, die zum Konfigurieren von Sicherheitsrichtlinien und Sicherheits Zuordnungen verwendet werden. Erstellt *filename*. SPD für Sicherheitsrichtlinien und *Dateiname*. sad für Sicherheits Zuordnungen. Verwenden Sie die erstellten Dateien als Vorlagen, um Sicherheitsrichtlinien oder Sicherheits Zuordnungen zu konfigurieren. Die Dateien können mit einem Text-Editor geändert werden. Um die in den SPD-und Sad-Dateien enthaltene Konfiguration aufzurufen, verwenden Sie den Befehl **dem ipsec6 a** .

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**dem ipsec6 a \[** _Dateiname (ohne Erweiterung)_*_\]_*
</dt> <dd>

Fügt der Liste der aktiven Sicherheitsrichtlinien und Sicherheits Zuordnungen Sicherheitsrichtlinien in *filename*. SPD und Sicherheits Zuordnungen in *filename*. Sad hinzu.

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**dem ipsec6 i \[**  *_Richtlinien \] \[_* _Dateiname (ohne Erweiterung)_*_\]_*
</dt> <dd>

Fügt der Liste aktiver Sicherheitsrichtlinien und Sicherheits Zuordnungen, auf die durch die Richtlinien Nummer verwiesen wird, Sicherheitsrichtlinien in *filename*. SPD und Sicherheits Zuordnungen in *filename*. Sad hinzu.

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**dem ipsec6 d \[ Type = SP SA \] \[** _indexnumber_*_\]_*
</dt> <dd>

Löscht Sicherheitsrichtlinien oder Sicherheits Zuordnungen aus der Liste der aktiven Sicherheitsrichtlinien und Sicherheits Zuordnungen, wie von ihrer Indexnummer referenziert (angezeigt mit **dem ipsec6 sp** oder **dem ipsec6 SA**).

</dd> </dl>

 

 



