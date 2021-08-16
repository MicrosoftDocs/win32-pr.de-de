---
title: Behandeln von Uniform Resource Locators
description: Ein Uniform Resource Locator (URL) ist eine kompakte Darstellung des Speicherorts und der Zugriffsmethode für eine Ressource im Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419433c8a06b6243bf048896664a67da31a3c58d1d79eb6fea65f9fc99dbe63a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121870"
---
# <a name="handling-uniform-resource-locators"></a>Behandeln von Uniform Resource Locators

Ein Uniform Resource Locator (URL) ist eine kompakte Darstellung des Speicherorts und der Zugriffsmethode für eine Ressource im Internet. Jede URL besteht aus einem Schema (HTTP, HTTPS oder FTP) und einer schemaspezifischen Zeichenfolge. Diese Zeichenfolge kann auch eine Kombination aus einem Verzeichnispfad, einer Suchzeichenfolge oder einem Namen der Ressource enthalten. Die WinINet-Funktionen bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, zu unterbrechen und zu kanonisieren. Weitere Informationen zu URLs finden Sie unter [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).

Die URL-Funktionen arbeiten aufgabenorientiert. Der Inhalt und das Format der URL, die der Funktion übergeben wird, werden nicht überprüft. Die aufrufende Anwendung sollte die Verwendung dieser Funktionen nachverfolgen, um sicherzustellen, dass die Daten im vorgesehenen Format vorliegen. Beispielsweise würde die [**InternetCanonicalizeUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) das Zeichen "%" in die Escapesequenz "%25" konvertieren, wenn keine Flags verwendet werden. Wenn [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) für die kanonisierte URL verwendet wird, wird die Escapesequenz "%25" in die Escapesequenz "%2525" konvertiert, was nicht ordnungsgemäß funktioniert.

-   [Was ist eine kanonisierte URL?](#what-is-a-canonicalized-url)
-   [Verwenden der WinINet-Funktionen zum Verarbeiten von URLs](#using-the-wininet-functions-to-handle-urls)
-   [Kanonisieren von URLs](#what-is-a-canonicalized-url)
-   [Kombinieren von Basis- und relativen URLs](#combining-base-and-relative-urls)
-   [Auflisten von URLs](#cracking-urls)
-   [Erstellen von URLs](#creating-urls)
-   [Direkter Zugriff auf URLs](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>Was ist eine kanonisierte URL?

Das Format aller URLs muss der akzeptierten Syntax und Semantik entsprechen, um über das Internet auf Ressourcen zugreifen zu können. Kanonisierung ist der Prozess der Formatierung einer URL, um dieser akzeptierten Syntax und Semantik zu folgen.

Zeichen, die codiert werden müssen, enthalten alle Zeichen, die kein entsprechendes Grafikzeichen im US-ASCII-codierten Zeichensatz (hexadezimal 80-FF, , die nicht im US-ASCII-Codezeichensatz und hexadezimal 00-1F und 7F verwendet werden, die Steuerzeichen sind, Leerzeichen, "%" (wird zum Codieren anderer Zeichen verwendet) und unsichere Zeichen (<, >, ", \# , {, }, \| , , \\ ^, ~, \[ und \] ').

## <a name="using-the-wininet-functions-to-handle-urls"></a>Verwenden der WinINet-Funktionen zum Verarbeiten von URLs

In der folgenden Tabelle sind die URL-Funktionen zusammengefasst.



| Funktion                                                   | BESCHREIBUNG                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Kanonisiert die URL.                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Kombiniert Basis- und relative URLs.                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analysiert eine URL-Zeichenfolge in Komponenten.               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Erstellt eine URL-Zeichenfolge aus Komponenten.              |
| [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Beginnt mit dem Abrufen einer FTP-, HTTP- oder HTTPS-Ressource. |



 

## <a name="canonicalizing-urls"></a>Kanonisieren von URLs

Das Kanonisieren einer URL ist der Prozess, der eine URL, die unsichere Zeichen wie Leerzeichen, reservierte Zeichen und so weiter enthalten kann, in ein akzeptiertes Format konvertiert.

Die [**InternetCanonicalizeUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) kann verwendet werden, um URLs zu kanonisieren. Diese Funktion ist sehr aufgabenorientiert, daher sollte die Anwendung ihre Verwendung sorgfältig nachverfolgen. [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) überprüft nicht, ob die übergebene URL bereits kanonisiert ist und ob die zurückgegebene URL gültig ist.

Die folgenden fünf Flags steuern, [**wie InternetCanonicalizeUrl eine**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) bestimmte URL behandelt. Die Flags können in Kombination verwendet werden. Wenn keine Flags verwendet werden, codiert die Funktion die URL standardmäßig.



| Wert                     | Bedeutung                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ICU-BROWSERMODUS \_        | Codieren oder decodieren Sie keine Zeichen nach " " oder "?", und entfernen Sie nach "?" keine \# nach". Wenn dieser Wert nicht angegeben wird, wird die gesamte URL codiert, und nach dem Leerraum wird entfernt. |
| \_ICU-DECODIERUNG               | Konvertieren Sie alle %XX-Sequenzen in Zeichen, einschließlich Escapesequenzen, bevor die URL analysiert wird.                                                                                                          |
| NUR \_ ICU-CODIERUNGSRÄUME \_ \_ | Nur Leerzeichen codieren.                                                                                                                                                                                     |
| ICU \_ NO \_ ENCODE           | Konvertieren Sie unsichere Zeichen nicht in Escapesequenzen.                                                                                                                                                   |
| ICU \_ NO \_ META             | Entfernen Sie meta-Sequenzen (z.B. "." und "..") nicht aus der URL.                                                                                                                                       |



 

Das ICU-DECODE-Flag sollte nur für kanonisierte URLs verwendet werden, da davon ausgegangen wird, dass alle %XX-Sequenzen Escapecodes sind und diese in die vom Code angegebenen Zeichen \_ konvertiert. Wenn die URL ein "%"-Symbol enthält, das nicht Teil eines Escapecodes ist, behandelt ICU \_ DECODE sie weiterhin als eins. Dieses Merkmal kann dazu [**führen, dass InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine ungültige URL erstellt.

Um [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) zum Zurückgeben einer vollständig decodierten URL zu verwenden, müssen die \_ Flags ICU DECODE und ICU \_ NO \_ ENCODE angegeben werden. Bei diesem Setup wird davon ausgegangen, dass die URL, die an [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) übergeben wird, zuvor kanonisiert wurde.

## <a name="combining-base-and-relative-urls"></a>Kombinieren von Basis- und relativen URLs

Ein relative URL ist eine kompakte Darstellung des Speicherorts einer Ressource relativ zu einer absoluten Basis-URL. Die Basis-URL muss dem Parser bekannt sein und in der Regel das Schema, den Netzwerkspeicherort und Teile des URL-Pfads enthalten. Eine Anwendung kann [**InternetCombineUrl aufrufen,**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) um die relative URL mit ihrer Basis-URL zu kombinieren. [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) kanonisiert auch die resultierende URL.

## <a name="cracking-urls"></a>Auflisten von URLs

Die [**InternetCrackUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) trennt eine URL in ihre Komponententeile und gibt die Komponenten zurück, die durch die [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) angegeben sind, die an die Funktion übergeben wird.

Die Komponenten, aus denen sich die [**STRUKTUR DER \_ URL-KOMPONENTEN**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zusammenzieht, sind die Schemanummer, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen (z. B. Suchparameter). Jede Komponente, mit Ausnahme des Schemas und der Portnummern, verfügt über ein Zeichenfolgenelement, das die Informationen enthält, und einen Member, der die Länge des Zeichenfolgenelements enthält. Das Schema und die Portnummern verfügen nur über ein Member, das den entsprechenden Wert speichert. sie werden beide bei allen erfolgreichen Aufrufen von [**InternetCrackUrl zurückgegeben.**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)

Um den Wert einer bestimmten Komponente in der [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zu erhalten, muss der Member, der die Zeichenfolgenlänge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden. Der Zeichenfolgen-Member kann entweder die Adresse eines Puffers oder **NULL sein.**

Wenn der Zeiger member die Adresse eines Puffers enthält, muss der Zeichenfolgenlängen-Member die Größe dieses Puffers enthalten. [**InternetCrackUrl gibt**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) die Komponenteninformationen als Zeichenfolge im Puffer zurück und speichert die Zeichenfolgenlänge im Zeichenfolgenlängenelement.

Wenn der Zeiger member NULL **ist,** kann der Zeichenfolgenlängen-Member auf einen beliebigen Wert ungleich 0 (null) festgelegt werden. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) speichert die Adresse des ersten Zeichens der URL-Zeichenfolge, die die Komponenteninformationen enthält, und legt die Zeichenfolgenlänge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die sich auf die Komponente bezieht.

Alle Zeigermitglieder, die auf **NULL mit** einem Member ungleich 0 (null) festgelegt sind, zeigen auf den entsprechenden Ausgangspunkt in der URL-Zeichenfolge. Die im Längenelement gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.

Um die Initialisierung der [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) ordnungsgemäß zu beenden, muss das **dwStructSize-Member** auf die Größe der [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) in Bytes festgelegt werden.

Im folgenden Beispiel werden die Komponenten der URL im Bearbeitungsfeld IDC PreOpen1 und die Komponenten an das Listenfeld \_ IDC \_ PreOpenList zurückgegeben. Um nur die Informationen für eine einzelne Komponente anzuzeigen, kopiert diese Funktion das Zeichen unmittelbar nach den Komponenteninformationen in der Zeichenfolge und ersetzt es vorübergehend durch einen **NULL-Wert.**


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Erstellen von URLs

Die [**InternetCreateUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) verwendet die Informationen in der [**URL \_ COMPONENTS-Struktur,**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) um eine Uniform Resource Locator.

Die Komponenten, aus denen sich die [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zusammenzusetzen hat, sind das Schema, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen (z. B. Suchparameter). Jede Komponente, mit Ausnahme der Portnummer, verfügt über ein Zeichenfolgenelement, das die Informationen enthält, und einen Member, der die Länge des Zeichenfolgenelements enthält.

Für jede erforderliche Komponente sollte der Zeigerelement die Adresse des Puffers enthalten, der die Informationen enthält. Das Längenmitglied sollte auf 0 (null) festgelegt werden, wenn das Zeigermitglied die Adresse einer Zeichenfolge enthält, die auf Null endet. Der Längen-Member sollte auf die Zeichenfolgenlänge festgelegt werden, wenn der Zeiger member die Adresse einer Zeichenfolge enthält, die nicht mit 0 (null) beendet ist. Der Zeiger member aller Komponenten, die nicht erforderlich sind, muss **NULL sein.**

## <a name="accessing-urls-directly"></a>Direkter Zugriff auf URLs

Auf FTP- und HTTP-Ressourcen im Internet kann direkt mithilfe der [**Funktionen InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**InternetFindNextFile zugegriffen**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) werden. [**InternetOpenUrl öffnet**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) eine Verbindung mit der Ressource unter der URL, die an die Funktion übergeben wird. Wenn diese Verbindung hergestellt wird, gibt es zwei mögliche Schritte. Erstens: Wenn es sich bei der Ressource um eine Datei handelt, [**kann sie von InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) heruntergeladen werden. Zweitens: Wenn die Ressource ein Verzeichnis ist, [**kann InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) die Dateien im Verzeichnis aufzählen (außer bei Verwendung von CERN-Proxys). Weitere Informationen zu [**InternetReadFile finden Sie**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)unter [Lesen von Dateien.](common-functions.md) Weitere Informationen zu [**InternetFindNextFile finden**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)Sie unter [Suchen der nächsten Datei.](common-functions.md)

Für Anwendungen, die über einen CERN-Proxy betrieben werden müssen, kann [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) für den Zugriff auf FTP-Verzeichnisse und -Dateien verwendet werden. Die FTP-Anforderungen werden so verpackt, dass sie wie eine HTTP-Anforderung aussehen, die der CERN-Proxy akzeptiert.

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet das [**HINTERNET-Handle,**](appendix-a-hinternet-handles.md) das von der [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellt wurde, und die URL der Ressource. Die URL muss das Schema (http:, ftp:, file: \[ für eine lokale Datei oder \] https: für \[ sicheres Hypertextprotokoll) und den \] Netzwerkspeicherort (z. `www.microsoft.com` B. ) enthalten. Die URL kann auch einen Pfad enthalten (z.B. /isapi/gomscom.asp? TARGET=/windows/feature/) und Ressourcenname (z.B. default.htm). Für HTTP- oder HTTPS-Anforderungen können zusätzliche Header eingeschlossen werden.

[**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur HTTP- oder HTTPS-URLs) können das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellte Handle verwenden, um die Ressource herunterzuladen.

Das folgende Diagramm veranschaulicht, welche Handles mit den einzelnen Funktionen verwendet werden sollen.

![Handles für die Verwendung mit Funktionen](images/ax-wnt02.png)

Das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellte [**HINTERNET-Stammhandle**](appendix-a-hinternet-handles.md) wird von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet. Das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellte **HINTERNET-Handle** kann von [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (hier nicht gezeigt) und [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur HTTP- oder HTTPS-URLs) verwendet werden.

Weitere Informationen finden Sie unter [**HINTERNET Handles**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 