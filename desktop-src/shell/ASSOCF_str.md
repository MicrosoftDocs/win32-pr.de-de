---
description: Stellt Informationen für die iqueryassociations-Schnittstellen Methoden bereit.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Assocf-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219045"
---
# <a name="assocf-enumeration"></a>Assocf-Enumeration

Stellt Informationen für die [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Schnittstellen Methoden bereit.

## <a name="syntax"></a>Syntax

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th>C++</th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a>Konstanten

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**assocf \_ None** 

Es sind keine der folgenden Optionen festgelegt.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**assocf \_ Init \_ noremapclsid** 

Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Schnittstellen Methoden an, keine CLSID-Werte ProgID-Werten zuzuordnen.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**assocf \_ Init \_ byexename** 

Identifiziert den Wert des *pwszassoc* -Parameters von [**iqueryassociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) als Namen einer ausführbaren Datei. Wenn dieses Flag nicht festgelegt ist, wird der Stamm Schlüssel auf die ProgID festgelegt, die dem **exe** -Schlüssel anstelle der ProgID der ausführbaren Datei zugeordnet ist.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**\_zugeöffneter \_ byexename** 

Identisch mit " **assocf \_ Init \_ byexename**".

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**assocf \_ Init \_ defaultdestar** 

Gibt an, dass versucht wird, den vergleichbaren Wert aus dem Unterschlüssel abzurufen, wenn eine [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methode den angeforderten Wert nicht unter dem Stamm Schlüssel findet **\*** .

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**assocf \_ Init \_ defaultdefolder** 

Gibt an, dass versucht wird, den vergleichbaren Wert aus dem **Ordner** Unterschlüssel abzurufen, wenn eine [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methode den angeforderten Wert nicht unter dem Stamm Schlüssel findet.

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**assocf \_ nousersettings** 

Gibt an, dass nur **HKEY- \_ Klassen \_** Stamm gesucht werden sollen, und dass der **aktuelle HKEY- \_ \_ Benutzer** ignoriert werden soll.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**assocf- \_ NOTRUNCATE** 

Gibt an, dass die Rückgabe Zeichenfolge nicht abgeschnitten werden soll. Geben Sie stattdessen einen Fehlerwert und die erforderliche Größe für die gesamte Zeichenfolge zurück.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**assocf- \_ Überprüfung** 

Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methoden an, um zu überprüfen, ob die Daten korrekt sind. Diese Einstellung ermöglicht **iqueryassociations** -Methoden das Lesen von Daten von der Festplatte des Benutzers zur Überprüfung. Sie können z. b. den anzeigen Amen in der Registrierung anhand der in der exe-Datei gespeicherten Registrierung überprüfen. Wenn Sie dieses Flag festlegen, wird die Effizienz der Methode in der Regel reduziert.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**assocf \_ remaprundll** 

Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methoden an, Rundll.exe zu ignorieren und Informationen über das Ziel zurückzugeben. In der Regel geben **iqueryassociations** -Methoden Informationen über die erste exe-oder DLL-Datei in einer Befehls Zeichenfolge zurück. Wenn ein Befehl Rundll.exe verwendet, weist das Festlegen dieses Flags an, dass die Methode Rundll.exe ignoriert und Informationen über das Ziel zurückgibt.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**assocf- \_ nofixups** 

Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methoden an, keine Fehler in der Registrierung zu beheben, z. b. der Anzeige Name einer Funktion, die nicht mit der in der exe-Datei gefundenen Funktion übereinstimmt.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**assocf \_ ignorebaseclass** 

Gibt an, dass der BaseClass-Wert ignoriert werden soll.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**assocf \_ Init \_ ignoreunknown** 

**Eingeführt in Windows 7**. Gibt an, dass die "unbekannte" ProgID ignoriert werden soll. Führen Sie stattdessen einen Fehler aus.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**behobene von assocf \_ Init \_ \_** 

**Eingeführt in Windows 8**. Gibt an, dass die angegebene ProgID mithilfe der System Standardwerte anstelle der aktuellen Benutzer Standardwerte zugeordnet werden soll.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**"assocf" \_ ist \_ Protokoll** 

**Eingeführt in Windows 8**. Gibt an, dass der Wert ein Protokoll ist und mithilfe der aktuellen Benutzer Standardwerte zugeordnet werden soll.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**assocf- \_ Init \_ für \_ Datei** 

**Wurde in Windows 8.1 eingeführt**. Gibt an, dass die ProgID einer Datei Erweiterungs basierten Zuordnung entspricht. Verwenden Sie diese Verbindung mit der " **assocf init"- \_ \_ \_ ProgID**.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]               |
| Unterstützte Mindestversion (Server) | Windows 2000 Server \[nur Desktop-Apps\]                                 |
| Header                   |  Shlwapi. h  |



## <a name="see-also"></a>Weitere Informationen

 [**Assocquerykey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**assocquerystring**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**assocquerystringbykey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Alle Rechte vorbehalten.
