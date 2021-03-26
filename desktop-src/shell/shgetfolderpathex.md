---
UID: ''
title: Shgetfolderpathex-Funktion
description: Ruft den Pfad eines bekannten Ordners ab, der von der KNOWNFOLDERID identifiziert wird.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104976576"
---
# <a name="shgetfolderpathex-function"></a>Shgetfolderpathex-Funktion

## <a name="description"></a>BESCHREIBUNG

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.
Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ruft den vollständigen Pfad eines bekannten Ordners ab, der durch die [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)des Ordners identifiziert wird.
Dadurch wird " [shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) " erweitert, indem Sie die anfängliche Größe des Zeichen folgen Puffers festlegen können.

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>Parameter

### <a name="rfid-in"></a>RFID [in]

Ein Verweis auf die **KNOWNFOLDERID** , die den Ordner identifiziert.

### <a name="dwflags-in"></a>dwFlags [in]

Flags, die besondere Abruf Optionen angeben.
Dieser Wert kann 0 sein. andernfalls ein oder mehrere der [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) Werte.

### <a name="htoken-in-optional"></a>hToken [in, optional]

Ein [Zugriffs Token](/windows/desktop/SecAuthZ/access-tokens) , das einen bestimmten Benutzer darstellt.
Wenn dieser Parameter **null** ist, was die häufigste Verwendung ist, fordert die Funktion den bekannten Ordner für den aktuellen Benutzer an.

Fordern Sie den Ordner eines bestimmten Benutzers an, indem Sie das *hToken* dieses Benutzers übergeben.
Dies erfolgt in der Regel im Kontext eines Diensts, der über ausreichende Berechtigungen zum Abrufen des Tokens eines bestimmten Benutzers verfügt.
Dieses Token muss mit [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) und [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) Rechten geöffnet werden.
In einigen Fällen müssen Sie auch [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects)einschließen.
Zusätzlich zum Übergeben des *htokens* des Benutzers muss die Registrierungs Struktur dieses bestimmten Benutzers eingebunden werden.
Weitere Informationen zu Zugriffs Steuerungsproblemen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control) .

Beim Zuweisen des *hToken* -Parameters wird der Wert-1 für den Standardbenutzer angegeben.
Dies ermöglicht es Clients von [shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , Ordner Speicherorte (z. b. den **Desktop** Ordner) für den Standardbenutzer zu suchen.
Das Standardbenutzer Profil wird dupliziert, wenn ein neues Benutzerkonto erstellt wird, und enthält spezielle Ordner, z. b. **Dokumente** und **Desktop**.
Alle Elemente, die dem Standardbenutzer Ordner hinzugefügt werden, werden auch in jedem neuen Benutzerkonto angezeigt.
Beachten Sie, dass für den Zugriff auf die Standardbenutzer Ordner Administratorrechte erforderlich sind.

### <a name="pszpath-out"></a>pszpath [out]

Eine NULL terminierte Unicode-Zeichenfolge.
Dieser Puffer muss die Größe cchpath aufweisen.
Wenn " **shgetfolderpathex** " erfolgreich zurückgegeben wird, enthält dieser Parameter den Pfad für den bekannten Ordner.

### <a name="cchpath-in"></a>cchpath [in]

Die Größe des *ppszpath* -Puffers in Zeichen.

## <a name="returns"></a>Gibt zurück

Gibt **S_OK** zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Da [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ein Wrapper für [shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)ist, fungiert diese Funktion (**shgetfolderpathex**) auch als Erweiterung von **SHGetFolderPath**.

## <a name="see-also"></a>Weitere Informationen

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[Shgetknownfolderidlist](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[Shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
